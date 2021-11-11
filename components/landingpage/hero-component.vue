<template>
  <v-container fluid  class="bg">
    <section >
      <v-row
        :class="[
          $vuetify.breakpoint.mdAndUp ? 'mt-15' : 'mt-0',
          $vuetify.breakpoint.mdAndUp
            ? 'justify-space-between'
            : 'justify-center'
        ]"
      >
        <v-col cols="12" md="6" lg="5" class="ml-auto">
          <div class="hero__heading font-weight-black">
            The #1 Event Ticketing <br />
             Platform in Africa
          </div>

          <div class="my-2 grey--text font-weight-light font__16 ">
           Buy and sell tickets on the internet
          </div>
          <div class="my-6 accent--text font-weight-medium font__16">
           Create immersive virtual, hybrid, and in-person event experiences <br> for your audience, no matter where they are.
          </div>

          <div :class="[{ 'mt-9': $vuetify.breakpoint.xsOnly }]">
            <v-btn
              exact
              to="#"

               rounded depressed
               height="50"
              class="btn font__15 white--text font-weight-bold"
              :width="$vuetify.breakpoint.xsOnly ? '100%' : '150'"
              color="#FC6436"
              >Sign Up For Free</v-btn
            >
          </div>
        </v-col>
        <v-col
          md="6"
          :class="[{ 'd-none': $vuetify.breakpoint.smAndDown }]"
          lg="6"
        >
          <v-img
            loading="lazy"
            height="450"
            contain
            class="my-8"
            src="/images/hero-image-tix-2.png"
          />
        </v-col>
      </v-row>


    </section>
  </v-container>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>


.hero__heading {
  font-size: 40px;

  margin-top: 5rem;

  @media (max-width: 1024px) {
    font-size: 2rem;
  }

  @media (max-width: 425px) {
    font-size: 1.4rem;
    margin-top: 5rem;
  }
}


</style>
