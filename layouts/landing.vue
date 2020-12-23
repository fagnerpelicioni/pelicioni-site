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
  name: 'Landing'
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
