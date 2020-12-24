<template>
  <v-app dark>
    <v-container>
      <Header />
      <v-main>
        <v-container>
          <nuxt />
        </v-container>
      </v-main>
    </v-container>
  </v-app>
</template>

<script>
export default {
  name: 'Landing',

  created () {
    // eslint-disable-next-line no-console
    console.log('%cAntifa Action ⚐⚐', 'color: red; background: #000; padding:15px;')
  },

  head () {
    return {
      titleTemplate: 'Fagner Pelicioni',
      meta: [
        {
          hid: 'description',
          property: 'description',
          content: 'Desenvolvedor frontend e cientista da computação.'
        },
        {
          hid: 'og:description',
          property: 'og:description',
          content: 'Desenvolvedor frontend e cientista da computação.'
        },
        {
          hid: 'og:title',
          property: 'og:title',
          content: 'Fagner Pelicioni'
        },
        {
          hid: 'apple-mobile-web-app-title',
          property: 'apple-mobile-web-app-title',
          content: 'Fagner Pelicioni'
        },
        {
          hid: 'og:site_name',
          property: 'og:site_name',
          content: 'Fagner Pelicioni'
        },
        {
          hid: 'og:url',
          property: 'og:url',
          content: 'https://pelicioni.com.br'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
@import '@/assets/project.scss';

.theme--dark.v-application {
  background-color: var(--v-background-base);
}
.theme--light.v-application {
  background-color: var(--v-background-base);
}

.slide-bottom-enter-active,
.slide-bottom-leave-active {
  transition: opacity 0.25s ease-in-out, transform 0.25s ease-in-out;
}
.slide-bottom-enter,
.slide-bottom-leave-to {
  opacity: 0;
  transform: translate3d(0, 15px, 0);
}
</style>
