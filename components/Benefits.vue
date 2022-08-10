<template>
  <div class="benefits">
    <h2 class="text-center benefits_h1">Преимущества</h2>
    <div class="benefits__cards content-box">
      <v-row>
        <v-col
          v-for="(card, index) in cards"
          :key="`benefits__cards_${index}`"
          cols="12"
          md="6"
          sm="12"
        >
          <v-card class="benefits__cards__card">
            <v-row no-gutters class="nowrap">
              <v-img
                contain
                max-width="65px"
                :src="require(`@/assets/png/${card.src}`)"
                :lazy-src="require(`@/assets/png/${card.src}`)"
              />
              <v-row no-gutters class="ml-3">
                <v-col cols="12">
                  <h4>{{ card.text }}</h4>
                </v-col>
                <v-col cols="12">
                  {{ card.subtext }}
                </v-col>
              </v-row>
            </v-row>
          </v-card>
        </v-col>
      </v-row>
      <v-row>
        <v-col
          v-for="(card, index) in info_comp"
          :key="`benefits__cards_${index}`"
          cols="12"
          md="4"
          sm="6"
        >
          <v-row no-gutters class="nowrap benefits__cards__card">
            <v-img
              contain
              max-width="65px"
              :src="require(`@/assets/png/${card.src}`)"
              :lazy-src="require(`@/assets/png/${card.src}`)"
            />
            <v-row no-gutters class="ml-3">
              <v-col cols="12">
                <h4>{{ card.text }}</h4>
              </v-col>
              <v-col cols="12">
                {{ card.subtext }}
              </v-col>
            </v-row>
          </v-row>
        </v-col>
      </v-row>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BenefitsHome',
  data() {
    return {
      cards: [
        {
          src: 'like.png',
          text: 'Клиенторентированность',
          subtext:
            'Поможем решать мелкие вопросы бeсллатно, подскажем что делать в той или иной ситуации ',
        },
        {
          src: 'user-headphone.png',
          text: 'Качество',
          subtext:
            'У нас индивидуальный подход к каждому клиенту. Поддержка в любых социальных сетях!',
        },
        {
          src: 'cash.png',
          text: 'Гибкость',
          subtext:
            'Если вам не подходит ни один из наших тарифов. напишите нам и мы сконфигурируем уникальный тариф под ваши нужды! ',
        },
        {
          src: 'clock.png',
          text: 'Скорость',
          subtext:
            'Наша поддержка готова ответить на допросы клиентов н любое время. мы разрабатываем обширную базу Wiki',
        },
      ],
      info_comp: [
        {
          src: 'oblako.png',
          text: 'Процессор Ryzen 3600',
          subtext:
            'Наши сервера порадуют вас выскоим уровнем производительности благодаря мощному процессору с высокой частотой и большим объемом кэша третьего уровня.',
        },
        {
          src: 'oblako.png',
          text: 'Оперативная память на DDR4',
          subtext:
            'Увеличенная ло сравнению в DDR3 слоссбнхть и частота нашей памяти не позволит залагать вашему серверу!',
        },
        {
          src: 'oblako.png',
          text: 'SSD NVME диски',
          subtext:
            'Благодаря более высокой скорссти чтения- записи данных ваш сервер будет запускаться быстрее чем когда-либо',
        },
        {
          src: 'oblako.png',
          text: 'Удобная панель',
          subtext:
            'В вашем распоряжени будет Pterodactyl -лучшая игровая панель с удобным интерфейсом и уникальным oновленным дизайном.',
        },
        {
          src: 'oblako.png',
          text: 'Планировщик и Бэкапы',
          subtext:
            'Регулярные бэкапы не позволят вашему серверу выйти из строя, а умный планировщик будет делать их за вас рнулярно!',
        },
        {
          src: 'oblako.png',
          text: 'Множество способов оплаты',
          subtext:
            'Банковские карты, всевозможные кошельки. криптовалюта и даже система безопасной сделки. Все это вы сможете найти в нашем биллњге',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.benefits {
  background-color: #2ab5ec;
  //   padding: 60px 40px;
  color: white;
  @media screen and (max-width: 1024px) {
    padding: 10px;
  }
  &_h1 {
    font-size: 44px;
  }
  &__cards {
    &__card {
      padding: 10px;
    }
  }
}
</style>