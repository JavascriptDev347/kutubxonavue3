<template>
  <div>
    <div class="bg_img fw-bold" style="color: white; font-size: 45px">
      <p
        style="
          opacity: 1;
          display: flex;
          justify-content: center;
          text-align: center;
        "
      >
        {{ $t("title") }}
      </p>
    </div>
    <div
      style="max-width: 1600px"
      class="container d-flex justify-content-md-between mt-5 flex-column"
    >
      <div
        class="d-flex justify-content-md-around w-100 flex-wrap"
        style="margin-bottom: 30px"
      >
      
      <p style="text-algin:center;max-width: 1200px;font-size: 30px;">{{$t("TITLE")}}</p>
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
  .bg_img  {
    font-size: 24px !important;
  }
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
  opacity: 0.9;
}
</style>
