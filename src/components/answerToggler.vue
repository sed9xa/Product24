<template>
  <div class="answer__toggler">
    <div class="toggler__show">
      <div class="toggler__title-block">
        <div class="toggler__pic">
          <img class="toggler__pic-img" :src="answer.imgSrc" alt="" />
        </div>
        <h3
          class="toggler__title"
          :style="{ color: answer.active ? '#00C368' : '' }"
        >
          {{ answer.title }}
        </h3>
      </div>

      <img
        @click="this.$emit('textToggle', answer.id)"
        :class="{ rotated: answer.active }"
        src="@/assets/images/arrowIcon.svg"
        alt=""
        class="toggler__arrow"
      />
    </div>
    <div class="toggler__hide" v-if="answer.active">
      <p class="toggler__text">{{ answer.text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    answer: Object,
  },
};
</script>

<style>
.answer__toggler {
  padding: 15px 0;
}
.toggler__show {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.toggler__pic {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background-color: #e7ebf0;
  margin-right: 24px;
}
.toggler__pic-img {
}
.toggler__title-block {
  display: flex;
  align-items: center;
}
.toggler__title {
  font-weight: 700;
  font-size: 24px;
}
.toggler__arrow {
  cursor: pointer;
  transition: 0.2s;
}
.toggler__hide {
  transition: 0.2s;
}
.toggler__text {
  max-width: 560px;
  margin-left: 65px;
  text-align: left;
}
.rotated {
  transform: rotate(180deg);
}
@media (max-width: 800px) {
  .toggler__pic {
    display: none;
  }
  .toggler__title {
    font-size: 16px;
    text-align: left;
  }
  .toggler__text{
    margin-left: 0;
    margin-top: 10px;
    text-align: left;
  }
}
</style>
