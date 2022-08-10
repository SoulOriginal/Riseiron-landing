<template>
  <div>
    <div class="section-swiper-swiper-wrapper content-box pa-2">
      <div class="section-swiper-swiper-wrapper__card">
        <client-only>
          <div ref="swiper" class="swiper mySwiper swiper-container">
            <div class="swiper-wrapper">
              <div
                v-for="(element, index) in SliderItems"
                :key="`${index}__swiper-slide`"
                class="swiper-slide swiper-card rounded-lg pa-3"
              >
                123
              </div>
            </div>
          </div>
        </client-only>
        <div class="swiper-navigation-wrapper">
          <div class="swiper-pagination" />
          <div class="swiper-navigation-wrapper-arrows">
            <div class="swiper-button-prev">
              <img :src="require(`@/assets/png/left.png`)" alt="" />
            </div>
            <div class="swiper-button-next">
              <img :src="require(`@/assets/png/right.png`)" alt="" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Swiper, { Navigation, Pagination, EffectFade } from 'swiper'
import 'swiper/swiper.scss'
Swiper.use([Navigation, Pagination, EffectFade])
export default {
  name: 'SwiperTarifsHome',
  data() {
    return {
      SliderItems: [{}, {}, {}, {}],
    }
  },
  async mounted() {
    await this.$nextTick()
    await new Swiper(this.$refs.swiper, {
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
      },
      slidesPerView: 3,
      spaceBetween: 40,
      //   breakpoints: {
      //     // when window width is >= 320px
      //     320: {
      //       slidesPerView: 1.3,
      //       spaceBetween: 12,
      //     },
      //     // when window width is >= 480px
      //     480: {
      //       slidesPerView: 2,
      //       spaceBetween: 12,
      //     },
      //     // when window width is >= 640px
      //     768: {
      //       slidesPerView: 2.3,
      //       spaceBetween: 40,
      //     },
      //   },
      // effect: 'fade',
      pagination: {
        el: '.swiper-pagination',
        type: 'bullets',
        bulletClass: 'swiper-pagination-bullet',
        clickable: true,
      },
      // modules: [Navigation, Pagination, Autoplay]
    })
  },
}
</script>

<style lang="scss" scoped>
.swiper-card {
  background-color: white;
  border: 1px solid blue;
  max-width: 400px;
}
</style>