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
      <div class="berry__swiper">
        <h1 class="swiper__title">Lorem ipsum, dolor sit amet consectetur</h1>
        <swiper
        
          @swiper="onSwiper"
          @slideChange="onSlideChange"
          :loop="true"
          :modules="modules"
          :navigation="{ nextEl: '.nextArrow', prevEl: '.prevArrow' }"
          :pagination="{
            clickable: true,
            el: '.swiper-pagination',
          }"
          :slides-per-view="1"
          :space-between="50"
        >
          <swiper-slide class="berry__slider"
            ><berry-block :imgSrc="'headphones'"
              >Lorem ipsum dolor sit amet consectetur, adipisicing
              elit.</berry-block
            ></swiper-slide
          >
          <swiper-slide class="berry__slider"
            ><berry-block :imgSrc="'ellipseCircle'"
              >Lorem ipsum dolor sit amet consectetur, adipisicing
              elit.</berry-block
            ></swiper-slide
          >
          <swiper-slide class="berry__slider"
            ><berry-block :imgSrc="'pad'"
              >Lorem ipsum dolor sit amet consectetur, adipisicing
              elit.</berry-block
            ></swiper-slide
          >
          <swiper-slide class="berry__slider"
            ><berry-block :imgSrc="'ellipseCircle'"
              >Lorem ipsum dolor sit amet consectetur, adipisicing
              elit.</berry-block
            ></swiper-slide
          >
          <swiper-slide class="berry__slider"
            ><berry-block :imgSrc="'headphones'"
              >Lorem ipsum dolor sit amet consectetur, adipisicing
              elit.</berry-block
            ></swiper-slide
          >
          <swiper-slide class="berry__slider"
            ><berry-block :imgSrc="'circleSquare'"
              >Lorem ipsum dolor sit amet consectetur, adipisicing
              elit.</berry-block
            ></swiper-slide
          >

          <div class="prevArrow" @click="onSwiper"></div>
          <div class="swiper-pagination"></div>
          <div class="nextArrow"></div>
        </swiper>
      </div>
    </div>
  </main>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation, Pagination } from "swiper";
import "swiper/css";
import "swiper/scss";
import "swiper/scss/navigation";
import "swiper/scss/pagination";
import berryBlock from "./berryBlock.vue";
import productTitle from "./UI/productTitle.vue";
export default {
  components: { berryBlock, productTitle, Swiper, SwiperSlide },
  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper);
      
    };
    const onSlideChange = () => {
      console.log("slide change");
    };
    return {
      onSwiper,
      onSlideChange,
      modules: [Navigation, Pagination],
    };
  },
};
</script>

<style lang="scss">
.main {
  max-height: 950px;
  padding-top: 75px;
  background-repeat: no-repeat;
  background-position: center;
  background-image: url("@/assets/images/mainBg.png");
  padding-bottom: 70px;
}
.main__berry {
  max-width: 950px;
  margin: 70px auto 0;
}
.main__title-block {
  display: none;
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
.main__berry-img {
  height: 400px;
}
.main__berry-third {
  width: 450px;
  margin-top: -60px;
}
.berry__swiper {
  display: none;
}
.swiper {
  padding-bottom: 50px;
}
.swiper-pagination {
  width: 200px;
  height: 50px;
  margin: auto;
}
.nextArrow,
.prevArrow {
  width: 10px;
  height: 20px;
  background-image: url("@/assets/images/leftArrow.svg");
  background-size: contain;
  background-repeat: no-repeat;
  position: relative;
  cursor: pointer;
}
.nextArrow::after,
.prevArrow::after {
  width: 10px;
  height: 20px;
}
.nextArrow {
  transform: rotate(180deg);
  left: 70%;
  bottom: 18px;
}
.prevArrow {
  top: 25px;
  left: 30%;
}
.swiper-pagination-fraction,
.swiper-pagination-custom,
.swiper-horizontal > .swiper-pagination-bullets,
.swiper-pagination-bullets.swiper-pagination-horizontal {
  width: 150px;
  margin: auto;
}
.swiper-pagination {
  display: block;
  position: static;
  width: 150px;
  margin: auto;
  padding: 0;
  margin: 0;
  bottom: auto;
  height: auto;
}
.swiper-pagination-bullet {
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background: #ccced1;
}
.swiper-pagination-bullet-active {
  background: #a6abbd;
}

.slider__nav {
  display: flex;
  align-items: center;
  width: 150px;
}
@media (max-width: 1000px) {
  .main {
    padding-bottom: 0;
  }
  .main__berry {
    margin: 0;
  }
  .main__berry .berry__block {
    display: none;
  }
  .main__berry-first {
    display: none;
  }
  .main__berry-img {
    margin: auto;
  }
  .main__berry-third {
    display: none;
  }
  .berry__slider .berry__block {
    margin: 0 auto 40px;
  }
  .swiper__title {
    margin: 0 15px 50px;
    font-size: 24px;
  }
  .berry__swiper {
    display: block;
  }
}
@media (max-width: 700px) {
  .main__berry-img {
    height: 200px;
  }
}
</style>
