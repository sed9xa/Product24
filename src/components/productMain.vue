<template>
  <main class="main">
    <div class="main__inner">
      <product-title class="main__title-block"
        >Lorem ipsum dolor sit amet consectetur.</product-title
      >
      <div class="main__berry">
        <div class="main__berry-first main__berry-block">
          <berry-block :imgSrc="'headphones'"
            >Lorem ipsum dolor sit amet consectetur, adipisicing
            elit.</berry-block
          >
          <berry-block :imgSrc="'ellipseCircle'"
            >Lorem ipsum dolor sit amet consectetur, adipisicing
            elit.</berry-block
          >
        </div>
        <div class="main__berry-second main__berry-block">
          <berry-block :imgSrc="'pad'"
            >Lorem ipsum dolor sit amet consectetur, adipisicing
            elit.</berry-block
          >
          <img
            class="main__berry-img"
            src="@/assets/images/mainBerry.png"
            alt=""
          />
          <berry-block :imgSrc="'ellipseCircle'"
            >Lorem ipsum dolor sit amet consectetur, adipisicing
            elit.</berry-block
          >
        </div>
        <div class="main__berry-third main__berry-block">
          <berry-block :imgSrc="'headphones'"
            >Lorem ipsum dolor sit amet consectetur, adipisicing
            elit.</berry-block
          >
          <berry-block :imgSrc="'circleSquare'"
            >Lorem ipsum dolor sit amet consectetur, adipisicing
            elit.</berry-block
          >
        </div>
      </div>
      <swiper
        :slides-per-view="3"
        :space-between="50"
        @swiper="onSwiper"
        @slideChange="onSlideChange"
      >
        <swiper-slide>Slide 1</swiper-slide>
        <swiper-slide>Slide 2</swiper-slide>
        <swiper-slide>Slide 3</swiper-slide>
        ...
      </swiper>
    </div>
  </main>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import berryBlock from "./berryBlock.vue";
import productTitle from "./UI/productTitle.vue";
export default {
  components: { berryBlock, productTitle, Swiper, SwiperSlide },
};
</script>

<style>
.main {
  height: 950px;
  padding-top: 75px;
  background-repeat: no-repeat;
  background-position: center;
  background-image: url("@/assets/images/mainBg.png");
}
.main__berry {
  max-width: 950px;
  margin: 70px auto 0;
}
.main__berry-block {
  display: flex;
  margin: auto;
  align-items: center;
  justify-content: space-between;
}
.main__berry-first {
  width: 450px;
  margin-bottom: 20px;
}
.main__berry-second {
}
.main__berry-img {
  height: 400px;
}
.main__berry-third {
  width: 450px;
  margin-top: -60px;
}
</style>
