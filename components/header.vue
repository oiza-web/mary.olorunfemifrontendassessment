<template>
<main>
  <v-navigation-drawer height="530" width="100%" color="rgba(0, 0, 0, 0.9)" disable-resize-watcher v-model="sideNav.model" :clipped="$vuetify.breakpoint.lgAndUp" app>
    <div style="position: relative">
      <v-icon style="position: absolute; right: 10px; top: 10px;" @click="sideNav.model = false" color="white">mdi-close-circle</v-icon>
    </div>

    <v-sheet tile color="transparent" class="py-3 mt-12 mb-5 d-flex justify-center">
      <nuxt-link to="/">
        <img src="/images/tix-logo-mixed2.png" width="170" class="mx-auto">
      </nuxt-link>
    </v-sheet>

    <v-list shaped dense>
      <template v-for="item in items">
        <v-list-item color="cta" dark nuxt :to="item.to" :key="item.text">
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>
              {{ item.text }}
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </template>
    </v-list>
  </v-navigation-drawer>

  <v-app-bar :class="$vuetify.breakpoint.lgAndUp ? 'px-12'  : ''" flat color="transparent" absolute>
    <div style="width: 100%" class="d-flex align-center pt-10">
      <div class="d-flex logo__wrapper mr-auto justify-space-between align-center">
        <v-toolbar-title>
          <nuxt-link to="/">
            <img src="/images/tix-logo-mixed2.png" class="logo mx-auto">
          </nuxt-link>
        </v-toolbar-title>

        <v-app-bar-nav-icon v-if="this.$vuetify.breakpoint.mdAndDown" @click.stop="sideNav.model = !sideNav.model" class="primary--text"></v-app-bar-nav-icon>
        <!-- <v-app-bar-nav-icon v-if="this.$vuetify.breakpoint.mdAndDown"  class="primary--text"></v-app-bar-nav-icon> -->
      </div>
      <!-- Nav for web -->
      <div class="d-flex align-center" v-if="$vuetify.breakpoint.lgAndUp">
        <v-btn nuxt to="#" class="font__15   mr-4 primary--text  font-weight-bold" text>Products</v-btn>
        <v-btn nuxt to="#events" class="font__15 mr-4 primary--text  font-weight-bold" text>Events</v-btn>
        <v-btn nuxt to="#" class="font__15  mr-4 primary--text  font-weight-bold" text>Pricing</v-btn>
        <v-btn nuxt to="#" class="font__15  mr-8 primary--text  font-weight-bold" text>Contact</v-btn>
        <v-btn nuxt to="#" rounded depressed  class="mr-4 font__15  white--text font-weight-bold" color="#038595" width="150" height="50">Log In</v-btn>
        <v-btn nuxt to="#" rounded depressed  class="mr-4 font__15 white--text font-weight-bold" color="#FC6436"  width="180" height="50">Request Demo</v-btn>
      </div>
    </div>
  </v-app-bar>
</main>
</template>

<style lang="scss" scoped>
.v-btn {
  transition: 0.7s;
  color: black !important;
  // font-size: 0.6em !important;

  @media (min-width: 1380px) {
    // font-size: 1rem !important;
  }


}

.logo__wrapper {
  @media (max-width: 1264px) {
    width: 100%;
  }
}
a{
  text-decoration: none;
}
.logo {
  width: 200px;

  @media (max-width: 600px) {
    width: 100px;
  }
}
</style>

<script>
export default {
  data: () => ({
    sideNav: {
      model: false,
      type: 'persistent',
      clipped: false,
      floating: false,
      mini: false,
      stateless: true,
      scrolled: false
    },
    items: [{
        icon: 'mdi-home',
        text: 'HOME',
        to: '/'
      },
      {
        icon: 'mdi-information',
        text: 'PRODUCTS',
        to: '#'
      },
      {
        icon: 'mdi-newspaper',
        text: 'EVENTS',
        to: '#'
      },
      {
        icon: 'mdi-phone-message',
        text: 'CONTACT',
        to: '/contact'
      },
      {
        icon: 'mdi-book-open-page-variant',
        text: 'LOG IN',
        to: '/sign-in'
      },
      {
        icon: 'mdi-book-open-page-variant',
        text: 'REQUEST DEMO',
        to: '/sign-up'
      }
    ],
  })
}
</script>
