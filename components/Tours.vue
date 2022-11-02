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
        autoplay: false,
      },
    }
  },
}
</script>

<template>
  <div class="slider__hero">
    <VueSlickCarousel v-bind="settings">
      <div style="margin-top: 48px !important">
        <div>
          <h3>{{ $t('umrah') }}</h3>
          <p class="tours-text" style="margin-bottom: 25px">
            Hijriy 1444 yil<br />
            2022-2023 milodiy
          </p>
          <div class="tour-list">
            <div class="tour-econom">
              <p>1650 $</p>
              <span>{{ $t('from') }}</span>
              <p>10 {{ $t('day') }}</p>
            </div>
            <div class="tour-standart">
              <p>1750 $</p>
              <span>{{ $t('from') }}</span>
              <p>15 {{ $t('day') }}</p>
            </div>
            <div class="tour-premium">
              <p>2000 $</p>
              <span>{{ $t('from') }}</span>
              <p>15 {{ $t('day') }}</p>
            </div>
          </div>
        </div>
      </div>
      <div>
        <div>
          <h3>{{ $t('dubai') }}</h3>
          <div class="tour-list">
            <div class="tour-econom">
              <p>550 $</p>
              <span>dan boshlab</span>
              <p>10 kun</p>
            </div>
          </div>
        </div>
      </div>
      <div>
        <div>
          <h3>{{ $t('turkey') }}</h3>
          <div class="tour-list">
            <div class="tour-econom">
              <p>700 $</p>
              <span>dan boshlab</span>
              <p>10 kun</p>
            </div>
          </div>
        </div>
      </div>
      <div>
        <div>
          <h3>{{ $t('maldiv') }}</h3>
          <div class="tour-list">
            <div class="tour-econom">
              <p>1200 $</p>
              <span>dan boshlab</span>
              <p>10 kun</p>
            </div>
          </div>
        </div>
      </div>
      <div>
        <div>
          <h3>{{ $t('misr') }}</h3>
          <div class="tour-list">
            <div class="tour-econom">
              <p>700 $</p>
              <span>dan boshlab</span>
              <p>10 kun</p>
            </div>
          </div>
        </div>
      </div>
    </VueSlickCarousel>
  </div>
</template>

<style lang="scss">
.slider__hero {
  margin-top: 48px !important;
}

div {
  overflow: hidden;
  h3 {
    color: #11795f;
    font-size: 48px;
    text-align: center;
    margin: 0 auto;
    margin-bottom: 25px;
  }
}

.tours-text {
  color: #a87d32;
  font-style: italic;
  text-align: center;
}
.tour-list {
  display: flex;
  justify-content: space-evenly;
  margin-top: 20px;
}

.tour-econom {
  background: #11795f;
  color: #fff;
  width: 154px;
  height: 80px;
  border-radius: 5px;
  text-align: center;
  padding-top: 10px;
}
.tour-standart {
  background: #11795f;
  color: #fff;
  width: 154px;
  height: 80px;
  border-radius: 5px;
  text-align: center;
  padding-top: 10px;
}
.tour-premium {
  background: #11795f;
  color: #fff;
  width: 154px;
  height: 80px;
  border-radius: 5px;
  text-align: center;
  padding-top: 10px;
}

@media only screen and (max-width: 425px) {
  .tour-list {
    display: flex;
    flex-direction: column;
    margin: 0 auto;
  }

  .tour-econom {
    display: flex;
    margin: 0 auto;
    flex-direction: column;
    padding: 10px;
  }
  .tour-standart {
    margin-bottom: 20px;
    margin-top: 20px;
    display: flex;
    margin-left: 20px;
    flex-direction: column;
    padding: 10px;
  }
  .tour-premium {
    display: flex;
    margin: 0 auto;
    flex-direction: column;
    padding: 10px;
  }
}
</style>
