<template>
<v-app id="default-layout">
  <Header />

  <v-content class="white">
    <nuxt />
  </v-content>

  <Footer />
</v-app>
</template>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css?family=Allura&display=swap');

.main__footer {
  margin-top: 100px;

  @media (max-width: 1240px) {
    margin-top: unset;
  }
}
</style>

<script>
import Header from '@/components/header'
// import Footer from '@/components/Footer'

export default {
  components: {
    header,
    // Footer
  }
}
