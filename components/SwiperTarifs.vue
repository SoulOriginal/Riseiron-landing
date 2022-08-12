<template>
  <div class="content-box" style="position: relative">
    <div ref="swiper" class="swiper content-box">
      <div class="swiper-wrapper">
        <div
          v-for="(element, index) in SliderItems"
          :key="`${index}__swiper-slide`"
          class="swiper-slide"
        >
          <v-row no-gutters class="pa-3 swiper-card rounded-lg">
            <v-col cols="12">
              <h1 class="color-primary">
                {{ element.title }}
              </h1>
            </v-col>
            <v-col cols="12">
              {{ element.subtext }}
            </v-col>
            <v-row no-gutters class="gap15">
              <v-col cols="12">
                <v-card color="#f4f4f4" class="pa-2">
                  <v-row class="gap15">
                    <div class="square-icon bg-primary">
                      <v-icon color="white" size="30">mdi-cpu-64-bit</v-icon>
                    </div>
                    <h4 class="flex-center">{{ element.cpu }}</h4>
                  </v-row>
                </v-card>
              </v-col>
              <v-col cols="12">
                <v-card color="#f4f4f4" class="pa-2">
                  <v-row class="gap15">
                    <div class="square-icon bg-primary">
                      <v-icon color="white" size="30">mdi-chip</v-icon>
                    </div>
                    <h4 class="flex-center">{{ element.ram }}</h4>
                  </v-row>
                </v-card>
              </v-col>
              <v-col cols="12">
                <v-card color="#f4f4f4" class="pa-2">
                  <v-row class="gap15">
                    <div class="square-icon bg-primary">
                      <v-icon color="white" size="30">mdi-harddisk</v-icon>
                    </div>
                    <h4 class="flex-center">{{ element.ssd }}</h4>
                  </v-row>
                </v-card>
              </v-col>
              <v-col cols="12">
                <v-card color="#f4f4f4" class="pa-2">
                  <v-row class="gap15">
                    <div class="square-icon bg-primary">
                      <v-icon color="white" size="30">mdi-web</v-icon>
                    </div>
                    <h4 class="flex-center">
                      {{ element.internet }}
                    </h4>
                  </v-row>
                </v-card>
              </v-col>
              <v-row no-gutters>
                <v-btn block color="#0083ff"> Купить </v-btn>
              </v-row>
            </v-row>
          </v-row>
        </div>
      </div>
    </div>
    <!-- <div ref="swiper" class="swiper mySwiper swiper-container">
            <div class="swiper-wrapper">
              <div
                v-for="(element, index) in SliderItems"
                :key="`${index}__swiper-slide`"
                class="swiper-slide swiper-card rounded-lg pa-3"
              >
                <v-row>
                  <v-col cols="12">
                    <h1 class="color-primary">
                      {{ element.title }}
                    </h1>
                  </v-col>
                  <v-col cols="12">
                    {{ element.subtext }}
                  </v-col>
                  <v-row no-gutters class="gap15">
                    <v-col cols="12">
                      <v-card color="#f4f4f4" class="pa-2">
                        <v-row class="gap15">
                          <div class="square-icon bg-primary">
                            <v-icon color="white" size="30"
                              >mdi-cpu-64-bit</v-icon
                            >
                          </div>
                          <h4 class="flex-center">{{ element.cpu }}</h4>
                        </v-row>
                      </v-card>
                    </v-col>
                    <v-col cols="12">
                      <v-card color="#f4f4f4" class="pa-2">
                        <v-row class="gap15">
                          <div class="square-icon bg-primary">
                            <v-icon color="white" size="30">mdi-chip</v-icon>
                          </div>
                          <h4 class="flex-center">{{ element.ram }}</h4>
                        </v-row>
                      </v-card>
                    </v-col>
                    <v-col cols="12">
                      <v-card color="#f4f4f4" class="pa-2">
                        <v-row class="gap15">
                          <div class="square-icon bg-primary">
                            <v-icon color="white" size="30"
                              >mdi-harddisk</v-icon
                            >
                          </div>
                          <h4 class="flex-center">{{ element.ssd }}</h4>
                        </v-row>
                      </v-card>
                    </v-col>
                    <v-col cols="12">
                      <v-card color="#f4f4f4" class="pa-2">
                        <v-row class="gap15">
                          <div class="square-icon bg-primary">
                            <v-icon color="white" size="30">mdi-web</v-icon>
                          </div>
                          <h4 class="flex-center">
                            {{ element.internet }}
                          </h4>
                        </v-row>
                      </v-card>
                    </v-col>
                    <v-row no-gutters>
                      <v-btn block color="#0083ff"> Купить </v-btn>
                    </v-row>
                  </v-row>
                </v-row>
              </div>
            </div>
          </div> -->
    <div class="swiper-button-prev"></div>
    <div class="swiper-button-next"></div>
  </div>
</template>

<script>
import { Swiper, Navigation, Autoplay } from 'swiper'
// import 'swiper/swiper.scss'
import 'swiper/swiper-bundle.min.css'
export default {
  name: 'SwiperTarifsHome',
  data() {
    return {
      SliderItems: [
        {
          title: 'GS-1',
          subtext:
            'Виртуальный хостинг универсален и позволяет размещать проекты самой разной сложности не заботясь администрировании.',
          cpu: '0.5 vCore x 4200 MHz',
          ram: '2 GB RAM DDR4',
          ssd: '5 GB NVMe',
          internet: '100 Mbit/sec',
        },
        {
          title: 'GS-1',
          subtext:
            'Виртуальный хостинг универсален и позволяет размещать проекты самой разной сложности не заботясь администрировании.',
          cpu: '0.5 vCore x 4200 MHz',
          ram: '2 GB RAM DDR4',
          ssd: '5 GB NVMe',
          internet: '100 Mbit/sec',
        },
        {
          title: 'GS-1',
          subtext:
            'Виртуальный хостинг универсален и позволяет размещать проекты самой разной сложности не заботясь администрировании.',
          cpu: '0.5 vCore x 4200 MHz',
          ram: '2 GB RAM DDR4',
          ssd: '5 GB NVMe',
          internet: '100 Mbit/sec',
        },
        {
          title: 'GS-1',
          subtext:
            'Виртуальный хостинг универсален и позволяет размещать проекты самой разной сложности не заботясь администрировании.',
          cpu: '0.5 vCore x 4200 MHz',
          ram: '2 GB RAM DDR4',
          ssd: '5 GB NVMe',
          internet: '100 Mbit/sec',
        },
        {
          title: 'GS-1',
          subtext:
            'Виртуальный хостинг универсален и позволяет размещать проекты самой разной сложности не заботясь администрировании.',
          cpu: '0.5 vCore x 4200 MHz',
          ram: '2 GB RAM DDR4',
          ssd: '5 GB NVMe',
          internet: '100 Mbit/sec',
        },
        {
          title: 'GS-1',
          subtext:
            'Виртуальный хостинг универсален и позволяет размещать проекты самой разной сложности не заботясь администрировании.',
          cpu: '0.5 vCore x 4200 MHz',
          ram: '2 GB RAM DDR4',
          ssd: '5 GB NVMe',
          internet: '100 Mbit/sec',
        },
      ],
    }
  },
  mounted() {
    // eslint-disable-next-line no-new
    const SECOND = 1000 // milliseconds
    Swiper.use([Navigation, Navigation])
    // init Swiper:
    // eslint-disable-next-line no-new
    new Swiper(this.$refs.swiper, {
      // configure Swiper to use modules
      modules: [Autoplay],
      slidesPerView: 3,
      spaceBetween: 40,
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
      },
      loop: true,
      autoplay: {
        delay: 3 * SECOND,
        disableOnInteraction: false,
      },
      breakpoints: {
        // when window width is >= 320px
        320: {
          slidesPerView: 1,
          spaceBetween: 12,
        },
        768: {
          slidesPerView: 2,
          spaceBetween: 12,
        },
        // when window width is >= 640px
        1000: {
          slidesPerView: 3,
          spaceBetween: 20,
        },
        1440: {
          slidesPerView: 3,
          spaceBetween: 40,
        },
      },
      // Events
      on: {
        slideChange: (swiper) => {
          this.activeIndex = swiper.realIndex
        },
      },
    })
    // const swiper = new Swiper(this.$refs.swiper, {
    //   navigation: {
    //     nextEl: '.swiper-button-next',
    //     prevEl: '.swiper-button-prev',
    //   },
    //   slidesPerView: 3,
    //   spaceBetween: 40,
    //   breakpoints: {
    //     // when window width is >= 320px
    //     320: {
    //       slidesPerView: 3,
    //       spaceBetween: 12,
    //     },
    //     // when window width is >= 480px
    //     480: {
    //       slidesPerView: 1,
    //       spaceBetween: 12,
    //     },
    //     // when window width is >= 640px
    //     768: {
    //       slidesPerView: 3,
    //       spaceBetween: 40,
    //     },
    //   },
    //   // effect: 'fade',

    //   // modules: [Navigation, Pagination, Autoplay]
    // })
    // console.log(swiper)
  },
}
</script>

<style lang="scss" scoped>
.swiper-button-next {
  right: -50px;
  left: auto;
}
@media screen and (max-width: 960px) {
  .swiper-button-next,
  .swiper-button-prev {
    display: none;
  }
}
.swiper-button-prev {
  left: -50px;
  right: auto;
}
.swiper {
  overflow: hidden;
  position: relative;
}
.swiper-slide {
  align-items: center;
  display: flex;
  justify-content: center;
}
.square-icon {
  padding: 8px;
  border-radius: 12px;
}
.bg-primary {
  background-color: #0083ff;
}
.color-primary {
  color: #0083ff;
}
.swiper-card {
  background-color: white;
  -webkit-box-shadow: inset 0px 0px 0px 2px #0083ff;
  box-shadow: inset 0px 0px 0px 2px #0083ff;
}

.flex-center {
  display: flex;
  align-items: center;
}
.v-btn--block {
  min-width: unset !important;
}
</style>