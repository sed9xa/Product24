<template>
  <product-nav></product-nav>
  <product-main></product-main>
  <footer class="footer">
    <product-blog class="footer__blog"></product-blog
    ><product-answers class="footer__answers"></product-answers>
  </footer>
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
.footer {
  display: flex;
  min-height: 830px;
}
@media (max-width: 1400px) {
  .footer {
    flex-direction: column-reverse;
  }
  .footer__blog {
    width: 100%;
  }
  .footer__answers {
    width: 100%;
    min-height: 700px;
  }
}
</style>
