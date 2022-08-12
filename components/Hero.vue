<template>
  <div id="scrolling-techniques-7" class="hero">
    <v-row class="content-box" style="height: 100%">
      <v-col cols="12" md="6" sm="12" class="hero__conteiner_text">
        <div>
          <div>
            <h1 class="hero__conteiner_text--h1">
              ГИБКИЙ ХОСТИНГ ПОД ЛЮБЫЕ ЗАДАЧИ
            </h1>
          </div>
          <div cols="12">
            <p>
              Универсальный хостинг для создания и размещения сайтов, серверов
              Minecraft и других игровых серверов. VDS и выделенных серверов
              любой сложности.
            </p>
          </div>
          <div cols="12">
            <v-row class="elements-gap">
              <v-btn dark>Техническая поддержка</v-btn>
              <v-btn>Создать сервер</v-btn>
            </v-row>
          </div>
        </div>
      </v-col>
      <v-col cols="12" md="6" sm="12" class="flex-end">
        <v-img
          class="hero-img"
          :lazy-src="require('@/assets/png/computer.png')"
          :src="require('@/assets/png/computer.png')"
        />
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: 'HeroComponent',
}
</script>

<style lang="scss" scoped>
.flex-end {
  display: flex;
  align-content: flex-end;
  align-items: flex-end;
  @media screen and (max-width: 660px) {
    display: block;
  }
}
.hero {
  right: 0;
  left: 0;
  height: 809px;
  background-color: #2ab5ec;
  &__conteiner_text {
    color: white;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    &--h1 {
      font-size: 44px;
    }
  }
  &-img {
    @media screen and (max-width: 660px) {
      max-width: 300px;
      margin: 0 auto;
    }
  }
}
</style>