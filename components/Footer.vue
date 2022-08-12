<template>
  <v-footer id="home-footer" padless color="mt-12" min-height="200">
    <div class="content-box h100">
      <div class="fluid-container h100">
        <div class="footer-content h100 w100">
          <div class="d-flex">
            <v-img max-width="60px" :src="require(`@/assets/png/logo.png`)" />
            <div class="d-flex column ml-3 justify-center">
              <strong class="text-center color-white">FLEXIBLE.HOST</strong>
              <div class="color-white">ГИБКИЙ ХОСТИНГ</div>
            </div>
          </div>
          <div></div>
          <div></div>
        </div>
      </div>
    </div>
  </v-footer>
</template>

<script>
export default {
  name: 'HomeFooter',

  data: () => ({}),
  computed: {
    socials() {
      return [
        {
          icon: 'mdi-facebook',
          link: 'https://www.facebook.com/oneclickmarine',
          color: '#3b5998',
        },
        {
          icon: 'mdi-instagram',
          link: 'https://www.instagram.com/oneclick_marine/',
          color: '#ffc273',
        },
        {
          icon: 'mdi-telegram',
          link: 'https://t.me/oneclickmarine',
          color: '#0088CC',
        },
        {
          icon: 'mdi-linkedin',
          link: 'https://www.linkedin.com/company/oneclickmarine/',
          color: '#007bb6',
        },
      ]
    },
  },
}
</script>

<style lang="scss">
#home-footer {
  background-image: url(data:image/svg+xml;base64,PHN2ZyBpZD0idmlzdWFsIiB2aWV3Qm94PSIwIDAgMTQ0MCAzMDAiIHdpZHRoPSIxNDQwIiBoZWlnaHQ9IjMwMCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayIgdmVyc2lvbj0iMS4xIj48cGF0aCBkPSJNMCAxMzZMMzQuMyAxNDEuM0M2OC43IDE0Ni43IDEzNy4zIDE1Ny4zIDIwNS44IDE0OS4zQzI3NC4zIDE0MS4zIDM0Mi43IDExNC43IDQxMS4yIDExMy4zQzQ3OS43IDExMiA1NDguMyAxMzYgNjE3IDE1NC41QzY4NS43IDE3MyA3NTQuMyAxODYgODIzIDE5MC4zQzg5MS43IDE5NC43IDk2MC4zIDE5MC4zIDEwMjguOCAxODcuMkMxMDk3LjMgMTg0IDExNjUuNyAxODIgMTIzNC4yIDE4MC43QzEzMDIuNyAxNzkuMyAxMzcxLjMgMTc4LjcgMTQwNS43IDE3OC4zTDE0NDAgMTc4TDE0NDAgMzAxTDE0MDUuNyAzMDFDMTM3MS4zIDMwMSAxMzAyLjcgMzAxIDEyMzQuMiAzMDFDMTE2NS43IDMwMSAxMDk3LjMgMzAxIDEwMjguOCAzMDFDOTYwLjMgMzAxIDg5MS43IDMwMSA4MjMgMzAxQzc1NC4zIDMwMSA2ODUuNyAzMDEgNjE3IDMwMUM1NDguMyAzMDEgNDc5LjcgMzAxIDQxMS4yIDMwMUMzNDIuNyAzMDEgMjc0LjMgMzAxIDIwNS44IDMwMUMxMzcuMyAzMDEgNjguNyAzMDEgMzQuMyAzMDFMMCAzMDFaIiBmaWxsPSIjMDA2NkZGIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0ibWl0ZXIiPjwvcGF0aD48L3N2Zz4=);
  background-position: center;
  -moz-background-size: 100%; /* Firefox 3.6+ */
  -webkit-background-size: 100%; /* Safari 3.1+ и Chrome 4.0+ */
  -o-background-size: 100%; /* Opera 9.6+ */
  background-size: 100%;
  background-color: #003f88;
  color: white;
  @media (max-width: 1440px) {
    background-position: bottom;
  }
}
.fluid-container {
  display: flex;
  align-items: center;
}
.footer-content {
  margin: 10px;
  max-height: 70px;
  display: flex;
  justify-content: space-between;
}
.v-footer {
  display: unset;
}
.column {
  flex-direction: column;
}
.color-white {
  color: white;
}
.h100 {
  height: 100%;
}
.w100 {
  width: 100%;
}
</style>
