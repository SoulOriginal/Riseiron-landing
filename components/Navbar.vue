<template>
  <div>
    <nav class="navbar">
      <div class="content-box">
        <div class="navbar__content">
          <v-img
            max-width="60px"
            :src="require(`@/assets/png/logo.png`)"
            :lazy-src="require(`@/assets/png/logo.png`)"
          />
          <div class="hide-btn d-flex align-center">
            <v-btn text class="color-white">Главная</v-btn>
            <v-btn text class="color-white">О пректе</v-btn>
            <v-btn text class="color-white">Контакты</v-btn>
            <v-btn text class="color-white">Wiki</v-btn>
          </div>
          <div class="d-flex justify-center align-center">
            <v-button
              color="white"
              class="burger-btn"
              size="40"
              icon
              @click.stop="drawer = !drawer"
            >
              <v-icon>mdi-menu</v-icon>
            </v-button>
            <v-btn text class="color-white hide-btn">Вход</v-btn>
            <v-btn class="hide-btn">Регистрация</v-btn>
          </div>
        </div>
      </div>
    </nav>
    <v-navigation-drawer v-model="drawer" absolute temporary class="indexZ">
      <v-list>
        <v-list-item>
          <div class="w100">
            <div class="d-flex justify-center">
              <v-img
                max-width="60px"
                :src="require(`@/assets/png/logo.png`)"
                :lazy-src="require(`@/assets/png/logo.png`)"
              />
            </div>
          </div>
        </v-list-item>
        <v-list-item>
          <v-btn block text>Главная</v-btn>
        </v-list-item>

        <v-list-item>
          <v-btn block text>О пректе</v-btn>
        </v-list-item>

        <v-list-item>
          <v-btn block text>Контакты</v-btn>
        </v-list-item>

        <v-list-item>
          <v-btn block text>Wiki</v-btn>
        </v-list-item>

        <v-list-item>
          <v-btn block text>Войти</v-btn>
        </v-list-item>
        <v-list-item>
          <v-btn block>Регистрация</v-btn>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  name: 'HomeNavbar',
  data: () => ({
    appName: process.env.appName,
    drawer: false,
  }),
}
</script>

<style scoped lang="scss">
.indexZ {
  z-index: 123123123;
}
.w100 {
  width: 100%;
}
.hide-btn {
  @media (max-width: 840px) {
    display: none !important;
  }
}
.burger-btn {
  display: none;
  @media (max-width: 840px) {
    display: block;
  }
}
.navbar {
  position: fixed;
  width: 100%;
  background-color: #2ab5ec9e;
  z-index: 99999999;
  right: 0;
  &__content {
    padding: 25px 10px;
    @media (max-width: 840px) {
      padding: 10px 10px;
    }
    display: flex;
    justify-content: space-between;
  }
}
.color-white {
  color: white;
}
.profile-photo {
  width: 2rem;
  height: 2rem;
  margin: -0.375rem 0;
}
</style>
