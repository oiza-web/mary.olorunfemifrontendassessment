<template>
  <v-container fluid class="bg">
    <section class="boxed__container">
      <v-row
        :class="[
          $vuetify.breakpoint.mdAndUp ? 'mt-15' : 'mt-0',
          $vuetify.breakpoint.mdAndUp
            ? 'justify-space-around'
            : 'justify-center',
        ]"
      >
        <v-col
          md="6"
          :class="[{ 'd-none': $vuetify.breakpoint.smAndDown }]"
          lg="6"
        >
          <v-img
            loading="lazy"
            height="400"
            contain
            class="negative"
            src="/images/go-live.png"
          />
        </v-col>

        <v-col cols="12" md="6" lg="5" class="">
          <p class="font__40 font-weight-black primary--text">
            Go live in 5 minutes
          </p>

          <div class="my-4 primary--text font-weight-light font__16">
            Create, share and collect payments for live or virtual events <br />
            with our online ticketing tools.
          </div>

          <div :class="[{ 'mt-9': $vuetify.breakpoint.xsOnly }]">
            <v-btn
              exact
              to="#"
              depressed
              rounded
              class="
                text-capitalize
                btn
                font__15
                white--text
                font-weight-bold
                mt-4
              "
              :width="$vuetify.breakpoint.xsOnly ? '100%' : '150'"
              height="50"
              color="#038595"
              >Sign up for free</v-btn
            >
          </div>
        </v-col>
      </v-row>
    </section>
  </v-container>
</template>
<style lang="scss" scoped>
.bg {
  background-color: #f4f7fe;
}
.negative{
  margin-bottom: -14px;
}
</style>
