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
</style>
