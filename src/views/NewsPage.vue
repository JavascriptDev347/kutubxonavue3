<template>
  <div v-if="show">
    <form
      @submit.prevent="searchedProducts"
      class="d-flex w-50 justify-content-center"
      style="gap: 10px; margin-top: 20px"
    >
      <input
        type="text"
        class="form-control w-100"
        placeholder="Search news"
        v-model="searchQuery"
      />
    </form>

    <div
      class="container mt-4 d-flex flex-wrap justify-content-between justify-content-sm-center"
      style="gap: 30px; margin-bottom: 30px"
    >
      <div
        class="card"
        style="width: 22rem"
        v-for="(item, index) in searchedProducts"
        :key="item"
      >
        <div class="card__img">
          <img
            class="card-img-top"
            :src="require(`../assets/news/${item.url}`)"
            alt="Card image cap"
          />
        </div>
        <div class="card-body">
          <p class="card-text text-center item__name">
            {{ item.name }}
          </p>
          <p class="card-text item__title">{{ item.title }}</p>
        </div>

        <RouterLink
          :to="`/news/${item.id}`"
          :id="item.id"
          class="router btn btn-primary w-100"
        >
          <span v-if="lang === 'uz'">To'liq Ma'lumot</span>
          <span v-else-if="lang === 'ru'">полная информация</span>
          <span v-else>Complete information</span>
        </RouterLink>
      </div>
    </div>
  </div>
  <div
    v-else
    class="container d-flex align-items-center justify-content-center mt-5"
  >
    <LoadingIcon />
  </div>
</template>
<script setup>
import { computed, ref } from "vue";
import LoadingIcon from "./LoadingIcon.vue";
import { useI18n } from "vue-i18n";
import { getCurrentInstance } from "vue";
import axios from "axios";

const root = getCurrentInstance();
const single = ref({});
const { t, locale } = useI18n();
const show = ref(false);
const lang = localStorage.getItem("lang");
const news = ref([]);

const getNewsUz = () => {
  if (lang === "uz") {
    axios
      .get("http://localhost:3000/news")
      .then((res) => {
        news.value = res.data;
      })
      .catch((er) => console.log(er));
  } else if (lang === "ru") {
    axios
      .get("http://localhost:3000/news_ru")
      .then((res) => {
        news.value = res.data;
      })
      .catch((er) => console.log(er));
  } else if (lang === "en") {
    axios
      .get("http://localhost:3000/news_en")
      .then((res) => {
        news.value = res.data;
      })
      .catch((er) => console.log(er));
  }
};

// searching
const searchQuery = ref("");

const searchedProducts = computed(() => {
  return news.value.filter((product) => {
    return (
      product.name.toLowerCase().indexOf(searchQuery.value.toLowerCase()) != -1
    );
  });
});

getNewsUz();

setTimeout(() => {
  show.value = true;
}, 500);
</script>

<style scoped>
.router {
  color: #fff;
  text-decoration: none;
  font-weight: 500;
}
.card:hover {
  cursor: pointer;
}
.card:hover .card__img img {
  transform: scale(1.2);
}
.card:hover .item__name {
  color: #46b2d0;
}

.card__img {
  overflow: hidden;
  height: 200px;
}

.card__img img {
  height: 100%;
  transition: all 0.25s ease;
}

.item__name {
  color: #1a1a1a;
  font-weight: 700;
  font-size: 14px;
}

.item__title {
  font-size: 12px;
}
</style>
