<template>
  <!-- Swiper -->
  <div class="swiper-container" ref="swiperContainer">
    <div class="swiper-wrapper">
      <div class="swiper-slide">
        <img :src="require(`@/assets/img/${img_list[0]}.jpg`)" alt="" />
      </div>
      <div class="swiper-slide">
        <img :src="require(`@/assets/img/${img_list[1]}.jpg`)" alt="" />
      </div>
      <div class="swiper-slide">
        <img :src="require(`@/assets/img/${img_list[2]}.jpg`)" alt="" />
      </div>
    </div>
    <!-- Add Nav Arrows -->
    <div class="swiper-button-prev"></div>
    <div class="swiper-button-next"></div>
  </div>
  <!-- END Swiper -->
</template>

<script>
import Swiper from 'swiper';

export default {
  mounted() {
    this.$nextTick(() => {
      const swiper = new Swiper('.swiper-container', {
        //  slidesPerView = width control
        slidesPerView: 2.7,
        spaceBetween: 20,
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev',
        },
        breakpoints: {
          // when window width is >= 320px
          100: {
            slidesPerView: 2,
            spaceBetween: 15,
            centeredSlides: true,
            initialSlide: 1,
          },
          // when window width is >= 640px
          640: {
            slidesPerView: 3,
            spaceBetween: 30,
          },
          // when window width is >= 1000px
          1000: {
            spaceBetween: 25,
            centeredSlides: false,
            initialSlide: 0,
          },
          // when window width is >= 1900px
          1900: {
            slidesPerView: 4,
            spaceBetween: 40,
          },
        },
      });
      swiper.init();
    });
  },
  props: ['img_list'],
};
</script>

<style lang="stylus" scoped>
// **do not apply width to swiper-wrapper
.swiper-container {
  // flex-grow: 1;
  display: flex;
  width: 100%;
  margin-top: 1em;
  padding: 0;
  position: relative;
  // border: solid thin green;
  overflow: hidden;

  .swiper-wrapper {
    // border: solid thin indigo;
    height: 25vh;
    display: flex;
    flex-direction: row;

    .swiper-slide {
      position: relative;
      // width: 4rem;
      height: 100%;
      // border: solid thin red;
      text-align: center;
      font-size: 18px;
      background: #222;
      /* Center slide text vertically */
      display: -webkit-box;
      display: -ms-flexbox;
      display: -webkit-flex;
      display: flex;
      -webkit-box-pack: center;
      -ms-flex-pack: center;
      -webkit-justify-content: center;
      justify-content: center;
      -webkit-box-align: center;
      -ms-flex-align: center;
      -webkit-align-items: center;
      align-items: center;
      border-radius: 6%;
      transition: all 0.3s ease-in-out;

      // display:none;
      img {
        width: 100%;
        height: 100%;
        filter: brightness(90%);
        border-radius: 5%;
        object-fit: cover;
      }
    }

    .swiper-slide:hover {
      transform: scale(0.96);
    }

    .swiper-slide:hover img {
      filter: grayscale(0);
    }
  }
}
</style>
