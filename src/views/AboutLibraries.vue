<template>
  <div class="about">
    <div class="select_library">
      <div v-for="tab in Tab_List" :key="tab.id">
        <p
          @click="onChangePage"
          :class="`${activeTab === tab.name && 'active-tab'}`"
        >
          {{ tab.label }}
        </p>
      </div>
    </div>
    <div class="libraries" v-show="activeTab === Tabs.Uzbek">
      <div class="library">
        <div class="library_name">
          {{ $t("alisher") }}
        </div>
        <div class="library_desc">
          <span>{{ $t("uzb_library") }}</span>
        </div>
        <div class="img_map">
          <div class="img">
            <img :src="milliy2" alt="" />
          </div>
          <div class="map">
            <iframe

             
frameborder='0' height='400px' width='600px' scrolling='no'
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2996.6349347013474!2d69.2722076153606!3d41.31680477927072!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38ae8b2a6565712d%3A0x790feb8933429946!2z0J3QsNGG0LjQvtC90LDQu9GM0L3QsNGPINCR0LjQsdC70LjQvtGC0LXQutCwINCj0LfQsdC10LrQuNGB0YLQsNC90LAg0LjQvC4g0JAuINCd0LDQstC-0Lg!5e0!3m2!1sru!2s!4v1655384596271!5m2!1sru!2s"
             
              style="border-radius: 10px;"
              allowfullscreen=""
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
            ></iframe>
          </div>
        </div>
      </div>
      <div class="library">
        <div class="library_name">
          {{ $t("Knowladge") }}
        </div>
        <div class="library_desc">
          <span>{{ $t("uzb_library") }}</span>
        </div>
        <div class="img_map">
          <div class="img">
            <img :src="bilim" alt="" />
          </div>
          <div class="map">
            <iframe

             
frameborder='0' height='400px' width='600px' scrolling='no'

              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2998.3356370540246!2d69.20365331535946!3d41.2797991792742!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38ae8b04b18eacf7%3A0xf2c2136cb57503d9!2sToshkent%20shahar%20%22Bilim%22%20axborot-kutubxona%20markazi!5e0!3m2!1sru!2s!4v1655384709496!5m2!1sru!2s"
            
              style="border-radius: 10px"
              allowfullscreen=""
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
            ></iframe>
          </div>
        </div>
      </div>
      <div class="library">
        <div class="library_name">
          {{ $t("Turon") }}
        </div>
        <div class="library_desc">
          <span>{{ $t("turon_desc") }}</span>
        </div>
        <div class="img_map">
          <div class="img">
            <img :src="turon" alt="" />
          </div>
          <div class="map">
            <iframe

             
frameborder='0' height='400px' width='600px' scrolling='no'

              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2996.0350367370743!2d69.24149211536103!3d41.32985147926949!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38ae5f0f994764bb%3A0xd8c204213646f027!2z0JjQvdGE0L7RgNC80LDRhtC40L7QvdC90L4t0LHQuNCx0LvQuNC-0YLQtdGH0L3Ri9C5INGG0LXQvdGC0YAgVFVST04!5e0!3m2!1sru!2s!4v1655384751554!5m2!1sru!2s"
            
              style="border-radius: 10px"
              allowfullscreen=""
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
            ></iframe>
          </div>
        </div>
      </div>
      <div class="library">
        <div class="library_name">
          {{ $t("children_library") }}
        </div>
        <div class="library_desc">
          <span>{{ $t("children_library_desc") }}</span>
        </div>
        <div class="img_map">
          <div class="img">
            <img :src="child" alt="" />
          </div>
          <div class="map">
            <iframe

             
frameborder='0' height='400px' width='600px' scrolling='no'

              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2996.852652233747!2d69.28756891536045!3d41.3120689792712!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38aef4d4ee8df0ef%3A0x993c4e899ec8bda1!2z0KDQtdGB0L_Rg9Cx0LvQuNC60LDQvdGB0LrQsNGPINC00LXRgtGB0LrQsNGPINCx0LjQsdC70L7RgtC10LrQsA!5e0!3m2!1sru!2s!4v1655385054215!5m2!1sru!2s"
            
              style="border-radius: 10px"
              allowfullscreen=""
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
            ></iframe>
          </div>
        </div>
      </div>
      <div class="library">
        <div class="library_name">
          {{ $t("Academy_of_Sciences_of_Uzbekistan") }}
        </div>
        <div class="library_desc">
          <span>{{ $t("Academy_of_Sciences_of_Uzbekistan_desc") }}</span>
        </div>
        <div class="img_map">
          <div class="img">
            <img :src="academy" alt="" />
          </div>
          <div class="map">
            <iframe

             
frameborder='0' height='400px' width='600px' scrolling='no'

              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2997.1058027652134!2d69.28434981536032!3d41.306561879271754!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38ae8ad515a743d3%3A0x39f0e8ce7ec381ea!2z0JDQutCw0LTQtdC80LjRjyDQndCw0YPQuiDQoNC10YHQv9GD0LHQu9C40LrQuCDQo9C30LHQtdC60LjRgdGC0LDQvQ!5e0!3m2!1sru!2s!4v1655386903392!5m2!1sru!2s"
            
              style="border-radius: 10px"
              allowfullscreen=""
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
            ></iframe>
          </div>
        </div>
      </div>
      <div class="library">
        <div class="library_name">
          {{ $t("Republican_Scientific_Pedagogical_Library") }}
        </div>
        <div class="library_desc">
          <span>{{
            $t("Republican_Scientific_Pedagogical_Library_desc")
          }}</span>
        </div>
        <div class="img_map">
          <div class="img">
            <img :src="pedagok" alt="" />
          </div>
          <div class="map">
            <iframe

             
frameborder='0' height='400px' width='600px' scrolling='no'

              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2997.2494579739177!2d69.24520041744384!3d41.30343650000002!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38ae8b7c8cdd829f%3A0xd50a34bff143b63b!2sRespublika%20Ilmiy%20pedagogika%20kutubxonasi!5e0!3m2!1sru!2s!4v1655386966150!5m2!1sru!2s"
            
              style="border-radius: 10px"
              allowfullscreen=""
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
            ></iframe>
          </div>
        </div>
      </div>
    </div>
    <div class="libraries" v-show="activeTab === Tabs.Jahon">
      <div class="library">
        <div class="library_name">
          {{ $t("Harvard") }}
        </div>
        <div class="library_desc">
          <span>{{ $t("Harvard_library") }}</span>
        </div>
        <div class="img_map">
          <div class="img">
            <img :src="harvard2" alt="" />
          </div>
          <div class="map">
            <iframe

             
frameborder='0' height='400px' width='600px' scrolling='no'

              src="https://www.google.com/maps/embed?pb=!1m23!1m12!1m3!1d11789.665909458767!2d-71.1292448180348!3d42.37627356697049!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!4m8!3e6!4m0!4m5!1s0x405c5d5ce903a40d%3A0x4464f3131a2a38c4!2z0JHQuNCx0LvQuNC-0YLQtdC60LAg0KTQsNC50L0g0JDRgNGC0YEsIEhhcnZhcmQgVW5pdmVyc2l0eSwgMTgwNSBDYW1icmlkZ2UgU3QgTGl0dGF1ZXIgQ2VudGVyLCBDYW1icmlkZ2UsIE1BIDAyMTM4LCDQodC-0LXQtNC40L3QtdC90L3Ri9C1INCo0YLQsNGC0Ys!3m2!1d42.376412099999996!2d-71.1182208!5e0!3m2!1sru!2s!4v1655391750666!5m2!1sru!2s"
            
              style="border-radius: 10px"
              allowfullscreen=""
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
            ></iframe>
          </div>
        </div>
      </div>
      <div class="library">
        <div class="library_name">
          {{ $t("MIT_Library") }}
        </div>
        <div class="library_desc">
          <span>{{ $t("MIT") }}</span>
        </div>
        <div class="img_map">
          <div class="img">
            <img :src="MIT" alt="" />
          </div>
          <div class="map">
            <iframe

             
frameborder='0' height='400px' width='600px' scrolling='no'

              src="https://www.google.com/maps/embed?pb=!1m16!1m12!1m3!1d23580.6234953442!2d-71.11865611164994!3d42.37283331788516!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!2m1!1sMIT%20University%20Library!5e0!3m2!1sru!2s!4v1655391939029!5m2!1sru!2s"
            
              style="border-radius: 10px"
              allowfullscreen=""
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
            ></iframe>
          </div>
        </div>
      </div>
      <div class="library">
        <div class="library_name">
          {{ $t("Oxword_library") }}
        </div>
        <div class="library_desc">
          <span>{{ $t("Oxword_library_desc") }}</span>
        </div>
        <div class="img_map">
          <div class="img">
            <img :src="oxword" alt="" />
          </div>
          <div class="map">
            <iframe

             
frameborder='0' height='400px' width='600px' scrolling='no'

              src="https://www.google.com/maps/embed?pb=!1m16!1m12!1m3!1d23580.62649617983!2d-71.11865613949699!3d42.372825325200104!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!2m1!1soxword%20university%20library!5e0!3m2!1sru!2s!4v1655392604999!5m2!1sru!2s"
            
              style="border-radius: 10px"
              allowfullscreen=""
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
            ></iframe>
          </div>
        </div>
      </div>
      <div class="library">
        <div class="library_name">
          {{ $t("Cambridge") }}
        </div>
        <div class="library_desc">
          <span>{{ $t("Cambridge_library") }}</span>
        </div>
        <div class="img_map">
          <div class="img">
            <img :src="cambridge" alt="" />
          </div>
          <div class="map">
            <iframe

             
frameborder='0' height='400px' width='600px' scrolling='no'

              src="https://www.google.com/maps/embed?pb=!1m16!1m12!1m3!1d23580.627496458303!2d-71.11865614877935!3d42.37282266097175!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!2m1!1scambridge%20university%20library!5e0!3m2!1sru!2s!4v1655393136402!5m2!1sru!2s"
            
              style="border-radius: 10px"
              allowfullscreen=""
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
            ></iframe>
          </div>
        </div>
      </div>
      <div class="library">
        <div class="library_name">
          {{ $t("John_Hopkins") }}
        </div>
        <div class="library_desc">
          <span>{{ $t("John_Hopkins_desc") }}</span>
        </div>
        <div class="img_map">
          <div class="img">
            <img :src="John_Hopkins" alt="" />
          </div>
          <div class="map">
            <iframe

             
frameborder='0' height='400px' width='600px' scrolling='no'

              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3086.162608842071!2d-76.624744879239!3d39.32990122355375!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89c804df8502f88d%3A0x303d58494fa04c66!2z0KPQvdC40LLQtdGA0YHQuNGC0LXRgiDQlNC20L7QvdGB0LAg0KXQvtC_0LrQuNC90YHQsA!5e0!3m2!1sru!2s!4v1655393588006!5m2!1sru!2s"
            
              style="border-radius: 10px"
              allowfullscreen=""
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
            ></iframe>
          </div>
        </div>
      </div>
      <div class="library">
        <div class="library_name">
          {{ $t("California") }}
        </div>
        <div class="library_desc">
          <span>{{ $t("California_desc") }}</span>
        </div>
        <div class="img_map">
          <div class="img">
            <img :src="california" alt="" />
          </div>
          <div class="map">
            <iframe

             
frameborder='0' height='400px' width='600px' scrolling='no'

              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3304.787081022419!2d-118.44365278520667!3d34.0749719805997!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x80c2bc6298955555%3A0xdf7600e5127f53ba!2sUniversity%20of%20California%20Los%20Angeles%3A%20Library%20Collections%2C%20Research%2C%20and%20Instructional%20Services!5e0!3m2!1sru!2s!4v1655393926302!5m2!1sru!2s"
            
              style="border-radius: 10px"
              allowfullscreen=""
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
            ></iframe>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import libraries from "@/assets/libraries.jpg";
import bilim from "@/assets/bilim.png";
import turon from "@/assets/turon2.jpg";
import academy from "@/assets/academy.jpg";
import pedagok from "@/assets/pedagok.jpg";
import child from "@/assets/child.jpg";
import MIT from "@/assets/MIT.jpg";
import oxword from "@/assets/oxword.jpg";
import harvard2 from "@/assets/harvard2.jpg";
import milliy2 from "@/assets/milliy2.jpg";
import cambridge from "@/assets/cambridge.jpg";
import John_Hopkins from "@/assets/John_Hopkins.jpg";
import california from "@/assets/california.jpg";
import { ref } from "vue";
const Tabs = ref({
  Uzbek: "O'zbekiston Kutubxonalari",
  Jahon: "Jahon Kutubxonalari",
});
const activeTab = ref(Tabs.value.Uzbek);
const Tab_List = ref([
  { label: "O'zbekiston Kutubxonalari", name: Tabs.value.Uzbek, id: 1 },
  { label: "Jahon Kutubxonalari", name: Tabs.value.Jahon, id: 2 },
]);
const onChangePage = () => {
  if (activeTab.value === Tabs.value.Uzbek) {
    activeTab.value = Tabs.value.Jahon;
  } else if (activeTab.value === Tabs.value.Jahon) {
    activeTab.value = Tabs.value.Uzbek;
  }
};
const changelibrary = ref(true);
</script>

<style scoped>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.about {
  width: 100%;
  margin-top: 20px;
  margin-bottom: 30px;
}
.select_library {
  background: #ffffff;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
flex-wrap: wrap;
  display: flex;
  align-items: center;
  text-align: center;
  justify-content: space-evenly;
  margin: 10px 0 10px 20px;
  padding-left: 20px;
  padding-right: 20px;
}
.select_library div {
  display: flex;
  /*margin-top: 15px;*/
}
.select_library div p {
  position: relative;
  display: flex;
  flex-direction: column;
  transition: 0.3s ease all;
  margin-top: 18px;
  cursor: pointer;
  font-weight: 400;
  font-family: "Roboto", sans-serif;
}
.select_library div p::after {
  content: "";
  margin-top: 15px;
  background-color: #b1040e;
  height: 3px;
  width: 0;
  transition: 0.3s;
}
.select_library div .active-tab::after {
  content: "";
  margin-top: 15px;
  background-color: #b1040e;
  height: 3px;
  width: 100%;
  transition: 0.3s;
}
.select_library div .active-tab {
  color: #b1040e;
  font-weight: 500;
  transition: none;
}
.select_library div p:hover:after {
  width: 100%;
}
.select_library div span {
  height: 0;
  width: 100%;
  margin-top: 10px;
  border: 2px solid #b1040e;
}
.libraries {
  width: 96%;
  margin-top: 20px;
  margin-left: 2%;
  display: flex;
  flex-direction: column;
}
.libraries .library {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 15px 0px;
}
.libraries .library .library_name {
  font-size: 25px;
  margin: 10px 0px;
  font-weight: 500;
  font-family: "Roboto", sans-serif;
}
.libraries .library .library_desc {
  text-align: center;
  font-size: 15px;
  font-weight: 400;
  font-family: "Roboto", sans-serif;
}
.libraries .library .img_map {
  width: 100%;
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  margin: 15px 0px;
  justify-content: center;
}
.libraries .library .img_map .img {
  width: 600px;
  height: 400px;
  margin: 10px 0px;
  margin-right: 60px;
}
.libraries .library .img_map .img img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 10px;
}
.libraries .library .img_map .map {
  margin: 10px 0px;
}

@media screen and (max-width:1312px) {
  .libraries .library .img_map {
    justify-content: center;
  }
  
}



  

</style>
