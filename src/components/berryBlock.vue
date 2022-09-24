<template>
  <div class="berry__block">
    <component :is="imgSrc"></component>
    <p class="berry__block-text"><slot></slot></p>
  </div>
</template>

<script>
import pad from '@/assets/images/mainIcons/pad.vue'
import ellipseCircle from '@/assets/images/mainIcons/ellipseSquare.vue'
import headphones from '@/assets/images/mainIcons/headphones.vue'
import circleSquare from '@/assets/images/mainIcons/circleSquare.vue'

export default {
  props: {
    imgSrc: String,
  },
  components:{
    pad, headphones, ellipseCircle, circleSquare
  }
};
</script>

<style>
.berry__block {
  max-width: 200px;
}
.berry__block-img{
  fill: green;
}
svg:hover rect,
svg:hover path,
svg:hover circle{
  transition: .2s;
  stroke:  #00C368;
}
</style>
