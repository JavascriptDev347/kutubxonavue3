<template>
  <div v-if="show">
    <div class="books">
      <h2>{{ $t("Books") }}</h2>
      <div class="items">
        <div class="item" v-for="item in books" :key="item.id">
          <router-link :to="`/singlebook/:${item.id}`" class="_btn">{{
            $t("read_more")
          }}</router-link>
          <img :src="item.volumeInfo.imageLinks.thumbnail" alt="#" />
        </div>
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
import axios from "axios";
import { ref } from "vue";
import LoadingIcon from "./LoadingIcon.vue";
const books = ref([]);
const b = ref();
const show = ref(false);

setTimeout(() => {
  show.value = true;
}, 500);

const getBooks = () => {
  axios
    .get("https://www.googleapis.com/books/v1/volumes?q=programming")
    .then((res) => {
      books.value = res.data.items;
      console.log(res.data.items, "items");
    });
};
getBooks();
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.books {
  width: 100%;
  margin-top: 20px;
  margin-bottom: 30px;
}

.books h2 {
  text-align: center;
}
.books .items {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  justify-content: center;
  margin-top: 25px;
}
.books .footer {
  margin-top: 300px;
}
.books .items .item {
  position: relative;
  width: 250px;
  height: 280px;
  margin: 15px;
  border: 1px solid #999;
  border-radius: 10px;
  overflow: hidden;
}
.books .items .item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 10px;
  cursor: pointer;
}
.books .items .item ._btn {
  position: absolute;
  top: -40px;
  left: 29%;
  z-index: 333;
  width: 120px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 1px solid #1ca7c0;
  border-radius: 10px;
  background-color: #fff;
  color: #1ca7c0;
  transition: all 0.5s ease-in-out;
  font-size: 16px;
  font-family: "Roboto", sans-serif;
  text-decoration: none;
}
.books .items .item:hover ._btn {
  position: absolute;
  top: 60px;
  left: 29%;
}
</style>
