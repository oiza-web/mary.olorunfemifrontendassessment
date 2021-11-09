<template>
  <v-container fluid class="bg">
    <section class="boxed__container">
      <v-row
        :class="[
          $vuetify.breakpoint.mdAndUp ? 'mt-15' : 'mt-0',
          $vuetify.breakpoint.mdAndUp
            ? 'justify-space-between'
            : 'justify-center',
        ]"
      >
        <v-col cols="12" md="6" lg="5" class="mx-auto">
          <div class="font__40 primary--text font-weight-black">
            Testimonials
          </div>

          <div class="my-4 primary--text font__16">
            Tix.africa is an amazing platform. I used it for my concert during
            covid and it was awesome. My tickets ere sold in due time. One thing
            that stood out for me was that I was able to sell not only tickets
            but shirts, caps and books to my audience. I will recommend
            tix.africa ALWAYS!
          </div>
          <div class="my-10">
            <div class="font__18 primary--text font-weight-bold">
              Opeoluwa Badmus
            </div>
            <div class="font__12 font-weight-light">Gbagada, Lagos</div>
          </div>
        </v-col>
        <v-col
          md="6"
          :class="[{ 'd-none': $vuetify.breakpoint.smAndDown }]"
          lg="6"
        >
          <v-img
            loading="lazy"
            height="500"
            class="negative mr-10"
            contain
            src="/images/tix-review2.png"
          />
        </v-col>
      </v-row>
    </section>
  </v-container>
</template>
<style scoped>
.bg {
  background-color: #feb6a0;
}
.negative {
  margin-bottom: -40px !important;
  z-index: 1;
}
</style>
