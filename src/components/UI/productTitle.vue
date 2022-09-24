<template>
  <div class="product__title-block">
    <hr class="product__line" />
    <h1 class="product__title"><slot></slot></h1>
  </div>
</template>

<script>
export default {};
</script>

<style>
.product__line {
  border-top: 4px solid #00c368;
  width: 184px;
  margin: auto;
}
.product__title {
  margin-top: 22px;
  font-weight: 700;
  font-size: 40px;
}
</style>
