<script>
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
// import Banner1 from '@assets/images/banner1.jpg'

export default {
  name: 'BannerComponent',
  components: { VueSlickCarousel },

  data() {
    return {
      settings: {
        dots: false,
        dotsClass: 'slick-dots custom-dot-class',
        edgeFriction: 0.35,
        infinite: true,
        speed: 500,
        slidesToShow: 1,
        slidesToScroll: 1,
        autoplay: true,
      },
      images: [
        {
          imgSrc: require('../assets/images/banner1.jpg'),
        },
        {
          imgSrc: require('../assets/images/banner2.jpg'),
        },
        {
          imgSrc: require('../assets/images/banner3.jpg'),
        },
        {
          imgSrc: require('../assets/images/banner4.jpg'),
        },
        // { image: Banner4 },
        // { image: Banner5 },
        // { image: Banner6 },
      ],
    }
  },
}
</script>

<template>
  <div class="slider__hero">
    <VueSlickCarousel v-bind="settings">
      <div v-for="(item, images) in images" :key="images">
        <div class="banner__hero">
          <img :src="item.imgSrc" alt="test" />
        </div>
      </div>
    </VueSlickCarousel>
  </div>
</template>

<style lang="scss">
.banner__hero {
  max-height: 440px;
  border-radius: 25px;
  margin-top: 0 auto;
  margin-top: 64px;
  img {
    width: 100%;
    height: 540px;
    object-fit: contain;
  }
}
</style>
