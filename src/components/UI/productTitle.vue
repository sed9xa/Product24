<template>
  <div class="main__title-block">
    <hr class="main__line" />
    <h1 class="main__title"><slot></slot></h1>
  </div>
</template>

<script>
export default {};
</script>

<style>
.main__line {
  border-top: 4px solid #00c368;
  width: 184px;
  margin: auto;
}
.main__title {
  margin-top: 22px;
  font-weight: 700;
  font-size: 40px;
}
</style>
