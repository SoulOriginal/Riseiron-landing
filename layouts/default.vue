<template>
  <v-app>
    <v-main>
      <Navbar />
      <v-fade-transition mode="out-in">
        <nuxt />
      </v-fade-transition>
    </v-main>
    <Footer />
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