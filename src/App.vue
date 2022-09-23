<template>
  <product-nav></product-nav>
  <product-main></product-main>
</template>

<script>
import productNav from "@/components/productNav.vue";
import productAnswers from "@/components/productAnswers.vue";
import productBlog from "@/components/productBlog.vue";
import productMain from "@/components/productMain.vue";

export default {
  name: "App",
  components: { productNav, productAnswers, productBlog, productMain },
};
</script>

<style lang="scss">
* {
  font-family: "Roboto", sans-serif;
  box-sizing: border-box;
  margin: 0;
}
h1,
h2,
h3 {
  padding: 0;
  margin: 0;
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2e3a59;
}
</style>
