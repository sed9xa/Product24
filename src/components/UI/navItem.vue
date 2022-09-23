<template>
  <button
    class="nav__button"
    :class="[disabled ? 'nav__button-disabled' : 'nav__button-active']"
  >
    <slot></slot>
  </button>
</template>

<script>
export default {
  props: {
    disabled: Boolean,
  },
};
</script>

<style>
.nav__button {
  cursor: pointer;
  background: none;
  border: none;
  padding: 4px 24px;
}
.nav__button-active {
  background: #00c368;
  box-shadow: 0px 8px 16px rgba(0, 195, 104, 0.4);
  border-radius: 8px;
  color: white;
}
.nav__button-disabled {
  color: #a6abbd;
}
</style>
