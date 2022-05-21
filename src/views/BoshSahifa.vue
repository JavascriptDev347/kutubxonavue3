<template>
  <div>
    <div class="bg_img fw-bold" style="color: white; font-size: 45px">
      Tashkent Axboroto Texnologiyalari Universiteti
    </div>
    <div
      style="max-width: 1600px"
      class="container d-flex justify-content-md-between mt-5 flex-column"
    >
      <div
        class="d-flex justify-content-md-around w-100 flex-wrap"
        style="margin-bottom: 30px"
      >
        <div class="d-flex flex-wrap w-100 wrap__item">
          <div
            class="col-1 d-flex justify-content-sm-center justify-content-md-start px-2 py-3"
          >
            <i
              class="fa-solid fa-users"
              style="font-size: 40px; color: #de5750"
            ></i>
          </div>
          <div class="col-4">
            <h4
              class="py-2 fw-bold"
              style="
                font-family: Source Sans Pro, Helvetica Neue, Helvetica, Arial,
                  sans-serif;
              "
            >
              {{ $t("student_enrollment") }}
            </h4>
            <p class="py-2">
              <span class="fw-bold" style="color: #de5750"> 7,645 </span
              >{{ $t("undergraduate") }}
            </p>
            <span class="py-2"
              ><span style="color: #de5750" class="fw-bold"> 9,292 </span>
              {{ $t("graduate") }}</span
            >
            <p class="py-2">{{ $t("situation") }}</p>
          </div>
          <div class="col-4 library">
            <h2 class="py-2">{{ $t("library_data") }}</h2>

            <ul class="px-4">
              <li>{{ $t("scientific_literature") }} 26660</li>
              <li>{{ $t("name_") }}/116709 {{ $t("copy") }};</li>
              <li>
                {{ $t("textbooks") }} 1542 {{ $t("name_") }}/40096
                {{ $t("copy") }};
              </li>
              <li>
                {{ $t("tutorials") }} 4822 {{ $t("name_") }}/166532
                {{ $t("copy") }};
              </li>
              <li>
                {{ $t("fiction") }} 11461 {{ $t("name_") }}/17407
                {{ $t("copy") }}
              </li>
            </ul>
          </div>
          <div class="col-3 img" style="padding: 20px">
            <img :src="require('@/assets/tatu1.jpg')" alt="fds" class="w-100" />
          </div>
        </div>
        <!-- 2 -->
        <div class="d-flex flex-wrap w-100 wrap__item">
          <div
            class="col-1 d-flex justify-content-sm-center justify-content-md-start px-2 py-3"
          >
            <i
              class="fa-solid fa-graduation-cap"
              style="font-size: 45px; color: #53284f"
            ></i>
          </div>
          <div class="col-4">
            <h4
              class="py-2 fw-bold"
              style="
                font-family: Source Sans Pro, Helvetica Neue, Helvetica, Arial,
                  sans-serif;
              "
            >
              {{ $t("faculty") }}
            </h4>
            <p class="py-2">
              <span class="fw-bold" style="color: #de5750"> 9 </span>
              {{ $t("faculty") }}
            </p>
            <span class="py-2"
              ><span style="color: #de5750" class="fw-bold"> 2288 </span>
              {{ $t("professor") }}</span
            >
            <p class="py-2">5:1 {{ $t("ratio") }}</p>
          </div>
          <div class="col-4 library">
            <h2 class="py-2">TATU</h2>

            <ul class="px-4">
              <li>{{ $t("tatu_info") }}</li>
              <li>{{ $t("tatu_info_2003") }}</li>
              <li>
                {{ $t("tatu_info_2005") }}
              </li>

              <li>
                {{ $t("tatu_info_2017") }}
              </li>
            </ul>
          </div>
          <div class="col-3 img" style="padding: 20px">
            <img :src="require('@/assets/tatu2.jpg')" class="w-100" alt="asd" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

@media screen and (max-width: 596px) {
  .wrap__item {
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }
  .library {
    width: 100%;
    text-align: center;
  }
  .img {
    width: 100%;
    display: flex;
    justify-content: center;
  }
}

.bg_img {
  width: 100%;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  background-image: url("../assets/library.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
