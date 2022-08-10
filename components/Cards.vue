<template>
  <v-row class="cards content-box">
    <v-col
      v-for="(card, index) in data"
      :key="`cards__card_${index}`"
      cols="12"
      md="3"
      sm="12"
    >
      <v-card class="rounded-xl">
        <v-img
          class="cards__img-card"
          :src="require(`@/assets/png/${card.src}`)"
          :lazy-src="require(`@/assets/png/${card.src}`)"
        >
          <div class="cards__img-card-content">
            <h2>{{ card.text }}</h2>
            <h3 class="mt-10">{{ card.subtext }}</h3>
          </div>
        </v-img>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'CardsMain',
  data() {
    return {
      data: [
        {
          src: 'minecraft.jpg',
          text: 'MINECRAFT И ДРУГИЕ ИГРОВЫЕ СЕРВЕРА',
          subtext:
            'Игровой хостинг с удобной панелью управления вашими игровыми серверами',
        },
        {
          src: 'server-1.jpg',
          text: 'ВИРТУАЛЬНЫЕ СЕРВЕРА',
          subtext:
            'VOS/VPS с полным доступом. для тех, кто хочет получить максимум возможностеи и разбирается в командной строке Linux ',
        },
        {
          src: 'server-2.jpg',
          text: 'ВЫДЕЛЕННЫЕ СЕРВЕРА',
          subtext:
            'Возможность выбора конфигурации и настройки сервера для эффективной работы с любыми проектами',
        },
        {
          src: 'internet.jpg',
          text: 'ДОМЕНЫ',
          subtext: 'Уникальный адрес сайта по низкой цене!',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.cards {
  &__img-card {
    height: 550px;
    @media screen and (max-width: 960px) {
      max-height: 250px;
    }
    // display: flex;
    // justify-content: space-between;
    // flex-direction: column;
    &-content {
      background-color: rgba(43, 28, 28, 0.73);
      text-align: center;
      height: 100%;
      width: 100%;
      padding: 30px;
      color: white;
    }
  }
}
</style>