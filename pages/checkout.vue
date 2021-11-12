<template>
  <main>
    <v-row no-gutters>
      <v-container fill-height>
        <v-container class="form__container">
          <nuxt-link class="mt-6" to="/">
            <v-img src="/images/tix-logo-mixed2.png" height="50" contain />
          </nuxt-link>
          <div class="title text-center mb-6 my-8">Checkout</div>

          <v-stepper v-model="e1">
            <v-stepper-header>
              <v-stepper-step :complete="e1 > 1" step="1" color="info">
                Kindly input your details
              </v-stepper-step>
              <v-divider></v-divider>

              <v-stepper-step :complete="e1 > 2" step="2" color="info">
                Review your order
              </v-stepper-step>

              <v-divider></v-divider>

              <v-stepper-step color="info" step="3"> Payment </v-stepper-step>
            </v-stepper-header>

            <v-stepper-items>
              <v-stepper-content step="1">
                <v-card elevation="0" class="mb-12" color="" height="500px">
                  <v-form ref="form" v-model="valid" lazy-validation>
                    <v-text-field
                      class="my-4"
                      v-model="name"
                      color="info"
                      :rules="nameRules"
                      label="Name"
                      required
                    ></v-text-field>
                    <v-text-field
                      class="my-4"
                      v-model="number"
                      color="info"
                      :rules="numberRules"
                      label="Phone Number"
                      required
                    ></v-text-field>

                    <v-text-field
                      class="my-4"
                      color="info"
                      v-model="email"
                      :rules="emailRules"
                      label="E-mail"
                      required
                    ></v-text-field>

                    <v-select
                      class="my-4"
                      color="info"
                      v-model="select"
                      :items="items"
                      :rules="[(v) => !!v || 'Item is required']"
                      label="How did you hear about us"
                      required
                    ></v-select>
                  </v-form>
                </v-card>

                <v-btn depressed rounded color="secondary" @click="e1 = 2">
                  Continue
                </v-btn>
              </v-stepper-content>

              <v-stepper-content step="2">
                <v-card elevation="0" class="mb-12" color="" height="500px">
                  <div>
                    <div class="font-weight-bold font__16 my-4">
                      Tickect Name - Jhonny Drille Christmas Concert
                    </div>
                    <v-img
                      src="/images/event1.jpg"
                      max-height="300"
                      max-width="300"
                    />
                    <div class="my-2 font-weight-bold font__16">
                      RSVP + Shirts
                    </div>
                    <v-select
                      class="my-2"
                      color="info"
                      v-model="select"
                      :items="items2"
                      :rules="[(v) => !!v || 'Item is required']"
                      label="Qantity"
                      required
                    ></v-select>
                    <div>
                      Order summary <v-divider></v-divider>
                      <p class="font-weight-bold font__20 my-2">
                        Total Price : $1500
                      </p>
                    </div>
                  </div>
                </v-card>

                <v-btn depressed rounded color="secondary" @click="e1 = 3">
                  Pay Now
                </v-btn>

                <!-- <v-btn @click="e1 = 2"> Back </v-btn> -->
              </v-stepper-content>

              <v-stepper-content step="3">
                <v-card class="mb-12" color="" height="500px">
                  <v-card-title
                    class="accent white--text font-weight-black title"
                  >
                    PAYMENT<br />
                    DETAILS<v-spacer></v-spacer>

                    <v-img
                      aspect-ratio="3.075"
                      max-height="40"
                      :src="URL_IMAGE"
                      position="right"
                      contain
                    />
                  </v-card-title>

                  <v-card-text class="pb-10">
                    <v-row>
                      <v-col cols="6">
                        <v-subheader
                          class="grey--text text--lighten-1 pl-0 subheader"
                          >CARDHOLDER’S NAME</v-subheader
                        >
                        <v-text-field
                          single-line
                          outlined
                          label="Johny Relative"
                          hide-details
                        />
                      </v-col>

                      <v-col cols="6">
                        <v-subheader
                          class="grey--text text--lighten-1 pl-0 subheader"
                          >CARD NUMBER</v-subheader
                        >
                        <v-text-field
                          single-line
                          outlined
                          color="info"
                          hide-details
                        />
                      </v-col>

                      <v-col col="4">
                        <v-subheader
                          class="grey--text text--lighten-1 pl-0 subheader"
                          >EXPIRY DATE</v-subheader
                        >
                        <v-select
                          :items="month"
                          label="Month"
                          outlined
                         color="info"
                        />
                      </v-col>

                      <v-col col="4">
                        <v-subheader
                          class="grey--text text--lighten-1 pl-0 subheader"
                        ></v-subheader>
                        <v-select
                          :items="year"
                          label="Year"
                          outlined
                          color="info"

                        />
                      </v-col>

                      <v-col col="4">
                        <v-subheader
                          class="grey--text text--lighten-1 pl-0 subheader"
                          >CVV</v-subheader
                        >
                        <v-text-field single-line outlined color="accent" />
                      </v-col>
                    </v-row>
                  </v-card-text>
                </v-card>

                <v-btn
                  depressed
                  rounded
                  color="secondary"
                  @click="notificationDialog = true"
                >
                  Complete
                </v-btn>

                <!-- <v-btn text>
           Back
          </v-btn> -->
              </v-stepper-content>
            </v-stepper-items>
          </v-stepper>
        </v-container>
      </v-container>
    </v-row>

    <v-dialog persistent v-model="notificationDialog" max-width="500">
      <v-sheet class="p__relative">
        <v-btn
          @click="notificationDialog = false"
          light
          icon
          class="close__btn white"
        >
          <v-icon>mdi-close</v-icon>
        </v-btn>

        <div class="text-center px-5 pt-12 pb-7">
          <div class="title font-weight-bold mb-2">Congratulations there!</div>
          <div>
            <v-img src="/images/success-modal2.png" contain />
          </div>
          <div class="info--text text--darken-2 font-weight-bold font__14">
            Kindly check your email your ticket.
          </div>
        </div>

        <div class="text-center px-5 pt-7 pb-12 primary">
          <div class="font-weight-bold white--text mb-5">
            Thank you for choosing tix.afica
          </div>
          <v-btn
            width="150"
            to="/#events"
            depressed
            rounded
            color="white"
            class="black--text font-weight-bold font__12"
            >View more events</v-btn
          >
        </div>
      </v-sheet>
    </v-dialog>
  </main>
</template>

<script>
export default {
  layout: 'checkout',
  data() {
    return {
      e1: 1,
      notificationDialog: false,
      number: '',
      name: '',
      numberRules: [
        (v) => !!v || 'Phone number is required',
        (v) => (v && v.length <= 15) || 'Name must be less than 15 characters',
      ],
      nameRules: [
        (v) => !!v || 'Name is required',
        (v) => (v && v.length <= 10) || 'Name must be less than 10 characters',
      ],
      email: '',
      emailRules: [
        (v) => !!v || 'E-mail is required',
        (v) => /.+@.+\..+/.test(v) || 'E-mail must be valid',
      ],
      select: null,
      items: [
        'Facebook',
        'LinkedIn',
        'Instagram',
        'Friends & Family',
        'Celebrity',
      ],
      items2: [
        '1',
        '2',
        '3',
        '4',
        '5',
        '6',
        '7',
        '8',
        '9',
        '10',
        '11',
        '12',
        '13',
      ],
      year: ['2021', '2022', '2023', '2024', '2025', '2026'],
      month: [
        'Jan',
        'Feb',
        'Mar',
        'Apr',
        'May',
        'Jun',
        'Jul',
        'Aug',
        'Sep',
        'Nov',
        'Dec',
      ],
      checkbox: false,
    }
  },

}
</script>

<style lang="scss" scoped>
.bg {
  background: linear-gradient(0deg, rgb(3, 133, 149), rgba(255, 185, 81, 0.7)),
    url('/images/tix-reviews.png');
  height: 100vh;
  background-size: cover;
  background-position-x: 20%;

  @media screen and (max-width: 600px) {
    height: 0;
  }
}

.title {
  font-weight: bold;
  font-weight: 700;
  font-size: 30px;
  line-height: 44px;
  letter-spacing: -1px;
  color: #343434;
  margin-bottom: 20px;
  position: relative;

  &::before {
    position: absolute;
    bottom: -5px;
    height: 4px;
    width: 27px;
    content: '';
    background-color: #fc6436;

    @media (max-width: 600px) {
      bottom: -10px;
    }
  }

  @media (max-width: 600px) {
    font-size: 24px;
    line-height: 24px;
  }
}

// .logo {
//   width: 100px;

//   @media (max-width: 600px) {
//     width: 80px;
//     margin-bottom: 40px;
//   }
// }

.form__container {
  @media (min-width: 1264px) {
    max-width: 900px !important;
    margin: 0 auto;
  }
}
</style>
