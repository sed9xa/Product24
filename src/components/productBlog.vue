<template>
  <section class="blog">
    <div class="blog__container">
      <div class="blog__inner">
        <product-title class="blog__title"
          >Lorem ipsum dolor sit amet, consectetur adipisicing
          elit.</product-title
        >
        <div class="blog__bigitem">
          <img
            class="bigitem__img"
            src="@/assets/images/blogPortrait.svg"
            alt=""
          />
          <div class="bigitem__content">
            <div class="bigitem__content-text">
              Lorem ipsum, dolor sit amet consectetur adipisicing elit.
              Laboriosam quas, aut consectetur animi autem aliquid consequuntur
              suscipit exercitationem laborum cupiditate magnam eaque quae
              deleniti, iste nisi expedita, provident excepturi officia! Porro
              ab rerum omnis magnam eligendi error nobis dolore? Porro ab rerum
              omnis magnam eligendi error nobis dolore? Porro ab rerum omnis
              magnam eligendi error nobis dolore?
            </div>
            <div class="bigitem__content-author">Jane Doe</div>
          </div>
        </div>
        <div class="blog__smallitems">
          <div class="blog__smallitem-left blog__smallitem">
            <div class="blog__smallitem-content">
              <div class="blog__smallitem-text">
                Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                Laboriosam quas, aut consectetur animi autem aliquid
              </div>
              <div class="blog__smallitem-author">Jane Doe</div>
            </div>

            <img
              src="@/assets/images/blogPortrait.svg"
              alt=""
              class="blog__smallitem-img"
            />
          </div>
          <div class="blog__smallitem-right blog__smallitem">
            <img
              src="@/assets/images/blogPortrait.svg"
              alt=""
              class="blog__smallitem-img"
            />
            <div class="blog__smallitem-content">
              <div class="blog__smallitem-text">
                Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                Laboriosam quas, aut consectetur animi autem aliquid
              </div>
              <div class="blog__smallitem-author">Jane Doe</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import productTitle from "./UI/productTitle.vue";
export default {
  components: { productTitle },
};
</script>

<style>
.blog {
  background-color: #f5f5f5;
  width: 50%;
}
.blog__container {
  margin: 70px 73px 0;
}
.blog__title {
  margin-bottom: 49px;
}
.blog__bigitem {
  display: flex;
  align-items: center;
  margin-bottom: 134px;
}

.bigitem__content {
  position: relative;
  text-align: left;
  line-height: 24px;
  padding-left: 70px;
}
.bigitem__content::after,
.bigitem__content::before {
  position: absolute;
  content: "";
  background-image: url("@/assets/images/commas.svg");
  width: 40px;
  height: 26px;
}
.bigitem__content::before {
  transform: rotate(180deg);
  left: 15px;
}
.bigitem__content::after {
  bottom: 0px;
  right: 15px;
}
.bigitem__content-text {
  margin-bottom: 15px;
}
.bigitem__content-author {
  font-weight: 600;
}
.blog__smallitems {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.blog__smallitem {
  display: flex;
  width: 49%;
}
.blog__smallitem-content {
  text-align: left;
  line-height: 24px;
}
.blog__smallitem-text {
  margin-bottom: 20px;
}
.blog__smallitem-author {
  font-weight: 600;
}
.blog__smallitem-img {
  height: 110px;
  transform: translateY(-5px);
  margin-right: 20px;
}
@media (max-width: 700px) {
  .blog__container {
    margin: 70px 15px;
  }
  .blog__bigitem {
    flex-direction: column;
    box-shadow: 0px 8px 16px rgba(0, 195, 104, 0.24);
    border-radius: 32px;
    padding-bottom: 15px;
  }
  .bigitem__content {
    padding: 0 10px;
  }
  .bigitem__content-text {
    text-align: center;
  }
  .bigitem__content-author {
    text-align: center;
  }
  .bigitem__content::after,
  .bigitem__content::before {
    background-image: url("@/assets/images/commasGray.svg");
    top: -20%;
  }
  
  .blog__smallitems {
    flex-direction: column-reverse;
  }
  .blog__smallitem {
    width: 100%;
    margin-bottom: 30px;
  }
}
@media (max-width:400px) {
  .bigitem__img{
    width: 100px;
    height: 100px;
  }
}
</style>
