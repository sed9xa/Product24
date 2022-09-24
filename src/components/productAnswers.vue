<template>
  <section class="answers">
    <div class="answers__container">
      <div class="answers__inner">
        <product-title class="answers__title"
          >Lorem ipsum, dolor sit adipisicing elit.</product-title
        >
        <p class="answers__subtitle">
          Porro ab rerum omnis magnam eligendi error nobis dolore?
        </p>
        <div class="answers__togglers">
          <answer-toggler
            v-for="answer in answers"
            :key="answer.id"
            :answer="answer"
            @textToggle="textToggle"
            class="answers__toggler"
          ></answer-toggler>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import answerToggler from "./answerToggler.vue";
import ProductTitle from "./UI/productTitle.vue";
export default {
  components: { answerToggler, ProductTitle },
  data() {
    return {
      answers: [
        {
          id: 1,
          title: "Lorem ipsum, dolor sit amet adipisicing elit.",
          text: "Lorem ipsum, dolor sit amet adipisicing elit.Laboriosam quas, aut consectetur animi autem aliquid consequuntur suscipit exercitationem laborum cupiditate magnam eaque quae delenit",
          imgSrc: require("@/assets/images/answersIcons/ellipseCircle.svg"),
          active: false,
        },
        {
          id: 2,
          title: "Lorem ipsum, dolor sit amet adipisicing elit.",
          text: "Lorem ipsum, dolor sit amet adipisicing elit.Laboriosam quas, aut consectetur animi autem aliquid consequuntur suscipit exercitationem laborum cupiditate magnam eaque quae delenit",
          imgSrc: require("@/assets/images/answersIcons/led.svg"),
          active: false,
        },
        {
          id: 3,
          title: "Lorem ipsum, dolor sit amet adipisicing elit.",
          text: "Lorem ipsum, dolor sit amet adipisicing elit.Laboriosam quas, aut consectetur animi autem aliquid consequuntur suscipit exercitationem laborum cupiditate magnam eaque quae delenit",
          imgSrc: require("@/assets/images/answersIcons/lightsOff.svg"),
          active: false,
        },
        {
          id: 4,
          title: "Lorem ipsum, dolor sit amet adipisicing elit.",
          text: "Lorem ipsum, dolor sit amet adipisicing elit.Laboriosam quas, aut consectetur animi autem aliquid consequuntur suscipit exercitationem laborum cupiditate magnam eaque quae delenit",
          imgSrc: require("@/assets/images/answersIcons/splitter.svg"),
          active: false,
        },
        {
          id: 5,
          title: "Lorem ipsum, dolor sit amet adipisicing elit.",
          text: "Lorem ipsum, dolor sit amet adipisicing elit.Laboriosam quas, aut consectetur animi autem aliquid consequuntur suscipit exercitationem laborum cupiditate magnam eaque quae delenit",
          imgSrc: require("@/assets/images/answersIcons/powerOff.svg"),
          active: false,
        },
      ],
    };
  },
  methods: {
    textToggle(id) {
      for (let i = 0; i < this.answers.length; i++) {
        //this.answers[i].active = false;
        if (this.answers[i].id === id) {
          console.log(this.answers[i].id, id, this.answers[i].active);
          if (this.answers[i].active === true) {
            this.answers[i].active = false;
          } else if (this.answers[i].active === false) {
            this.answers[i].active = true;
          }
        }
        else{
          this.answers[i].active = false;
        }
        
      }
    },
  },
};
</script>

<style>
.answers {
  background-color: #f8fbff;
  width: 50%;
}
.answers__container {
  margin: 70px 80px 0;
}
.answers__inner {
}
.answers__title {
  max-width: 500px;
  margin: 0 auto 15px;
}
.answers__subtitle {
  margin-bottom: 25px;
}
.answers__togglers {
}
.answers__toggler {
  border-bottom: 1px solid #e7ebf0;
}
.answers__toggler:last-child {
  border: none;
}
@media (max-width: 600px) {
  .answers__container{
    margin: 0 30px;
  }
}
</style>
