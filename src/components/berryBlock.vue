<template>
  <div class="berry__block">
    <img :src="imgSrc" alt="" class="berry__block-img" />
    <p class="berry__block-text"><slot></slot></p>
  </div>
</template>

<script>
export default {
  props: {
    imgSrc: String,
  },
};
</script>

<style>
.berry__block {
  max-width: 200px;
}
.berry__block-img {
}
.berry__block-text {
}
</style>
