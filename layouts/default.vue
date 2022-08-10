<template>
  <v-app>
    <v-main>
      <!-- <Navbar /> -->

      <!-- <v-app-bar
        id="home-app-bar"
        app
        fixed
        color="transparent"
        elevate-on-scroll
        scroll-target="#scrolling-techniques-7"
        elevation="1"
        class="content-box"
        height="64"
      >
        <nuxt-link to="/"> img </nuxt-link>
        <v-spacer />
        <v-btn> ВХОД </v-btn>
        <v-btn> РЕГИСТРАЦИЯ </v-btn>
      </v-app-bar> -->
      <v-fade-transition mode="out-in">
        <nuxt />
      </v-fade-transition>
    </v-main>
    <!-- <Footer /> -->
  </v-app>
</template>

<script>
export default {
  name: 'DefoultLayout',
}
</script>

<style lang="scss" scoped>
#home-app-bar {
  z-index: 100;
}
</style>