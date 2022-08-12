<template>
  <div class="content-box-sm pa-2">
    <h2 class="mb-2">FAQ</h2>
    <v-expansion-panels class="gap15">
      <v-expansion-panel v-for="(item, i) in 5" :key="i" class="rounded-lg">
        <v-expansion-panel-header>
          <strong> Техническая поддержка </strong>
        </v-expansion-panel-header>
        <v-expansion-panel-content>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat.
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>
  </div>
</template>

<script>
export default {
  name: 'FAQ',
}
</script>

<style>
</style>