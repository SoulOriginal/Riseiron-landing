<template>
  <div class="hero">
    <v-row class="content-box">
      <v-col cols="12" md="6" sm="12" class="hero__conteiner_text">
        <el-row>
          <el-col>
            <h1 class="hero__conteiner_text--h1">
              ГИБКИЙ ХОСТИНГ ПОД ЛЮБЫЕ ЗАДАЧИ
            </h1>
          </el-col>
          <el-col cols="12">
            <p>
              Универсальный хостинг для создания и размещения сайтов, серверов
              Minecraft и других игровых серверов. VDS и выделенных серверов
              любой сложности.
            </p>
          </el-col>
          <el-col cols="12">
            <v-row class="elements-gap">
              <v-btn dark>Техническая поддержка</v-btn>
              <v-btn>Создать сервер</v-btn>
            </v-row>
          </el-col>
        </el-row>
      </v-col>
      <v-col cols="12" md="6" sm="12">
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
.hero {
  right: 0;
  left: 0;
  height: 709px;
  background-color: #2ab5ec;
  height: 600px;
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
    @media screen and (max-width: 960px) {
      max-width: 500px;
      margin: 0 auto;
    }
  }
}
</style>