<template>
  <div>
    <v-app id="inspire">
      <v-main>
        <v-container>
          <Header></Header>
          <RouterView></RouterView>
        </v-container>
      </v-main>
    </v-app>
  </div>
</template>

<script>
import Header from '~/components/Header.vue'
export default {
  components: {
    Header
  }
}
</script>

<style lang="scss" scoped></style>