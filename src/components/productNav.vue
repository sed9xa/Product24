<template>
  <nav class="navbar">
    <div class="navbar__container">
      <div class="navbar__inner">
        <div class="navbar__links">
          <a href="#" class="navbar__logo">
            <img
              src="@/assets/images/logo.svg"
              alt=""
              class="navbar__logo-img"
            />
          </a>
          <div class="navbar__items">
            <nav-item
              @mouseenter="item.disabled = false"
              @mouseleave="item.disabled = true"
              class="navbar_item"
              v-for="item in navItems"
              :key="item.id"
              :disabled="item.disabled"
              >{{ item.text }}</nav-item
            >
          </div>
        </div>
        <nav-item class="navbar__exit">Button</nav-item>
      </div>
    </div>
  </nav>
</template>

<script>
import navItem from "@/components/UI/navItem.vue";
export default {
  data() {
    return {
      navItems: [
        { id: "1", text: "NavItem1", disabled: true },
        { id: "2", text: "NavItem2", disabled: true },
        { id: "3", text: "NavItem3", disabled: true },
      ],
    };
  },
  components: {
    navItem,
  },
};
</script>

<style>
.navbar {
  height: 160px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.navbar__container {
  margin: 0 4vw;
  flex-grow: 1;
}
.navbar__inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.navbar__links {
  display: flex;
  align-items: center;
}
.navbar__logo {
}
.navbar__logo-img {
}
.navbar__items {
  display: flex;
  height: 32px;
}
.navbar_item {
  margin-left: 8vw;
  transition: 0.2s;
}
.navbar__exit {
  height: 32px;
}
@media (max-width: 1000px) {
  .navbar_item {
    margin-left: 10px;
  }
}
@media (max-width: 800px) {
  .navbar_item {
    display: none;
  }
}
@media (max-width: 500px) {
  .navbar__exit {
    display: none;
  }
  .navbar__logo-img{
    width: 100%;
  }
}
</style>
