<template>
<main>
  <v-row no-gutters>
      <v-container fill-height >


        <v-container class="form__container">
           <nuxt-link class="mt-6" to="/">
          <v-img src="/images/tix-logo-mixed2.png" height="50"  contain/>
        </nuxt-link>
          <div class="auth__title text-center mb-6 my-8">Checkout</div>

          <!-- <v-stepper v-model="step">
            <v-stepper-header>
              <v-stepper-step :complete="step > 1" step="1"></v-stepper-step>

              <v-divider color="grey"></v-divider>

              <v-stepper-step :complete="step > 2" step="2"></v-stepper-step>
            </v-stepper-header>

            <v-stepper-items>
              <v-stepper-content step="1">
                <v-form ref="authForm1" v-model="authValid1" class="form__wrapper" @submit.prevent="next">
                  <v-select :rules="generalRules" :items="genders" item-text="displayName" item-value="name" class="font-weight-bold font__12" :dense="$vuetify.breakpoint.xsOnly" placeholder="I am a" v-model="gender" validate-on-blur />

                  <v-select :rules="generalRules" :items="genders" item-text="displayName" item-value="name" class="font-weight-bold font__12" :dense="$vuetify.breakpoint.xsOnly" placeholder="Looking for" v-model="genderInterest" validate-on-blur />
                  <v-select :rules="generalRules" :items="genders" item-text="displayName" item-value="name" class="font-weight-bold font__12" :dense="$vuetify.breakpoint.xsOnly" placeholder="Looking for" v-model="genderInterest" validate-on-blur />
                  <v-select :rules="generalRules" :items="genders" item-text="displayName" item-value="name" class="font-weight-bold font__12" :dense="$vuetify.breakpoint.xsOnly" placeholder="Looking for" v-model="genderInterest" validate-on-blur />


                  <v-btn type="submit" depressed block rounded color="primary" height="45" class="mt-12 font-weight-bold">Continue</v-btn>
                </v-form>
              </v-stepper-content>

              <v-stepper-content step="2">
                <v-form ref="authForm2" v-model="authValid2" class="form__wrapper" @submit.prevent="signup">
                  <v-text-field :rules="generalRules" v-model="firstName" placeholder="First Name" class="font__12 font-weight-bold" validate-on-blur />

                  <v-text-field :rules="generalRules" v-model="lastName" placeholder="Last Name" class="font__12 font-weight-bold" validate-on-blur />

                  <v-text-field :rules="emailRules" v-model="email" type="email" placeholder="Email" class="font__12 font-weight-bold" validate-on-blur />

                  <v-text-field :rules="generalRules" v-model="phone" type="tel" placeholder="Phone Number" class="font__12 font-weight-bold" validate-on-blur />

                  <v-text-field autocomplete="new-password" :rules="passwordRules" v-model="password" type="password" placeholder="Password" class="font__12 font-weight-bold" validate-on-blur />

                  <v-btn :loading="loading" type="submit" depressed block rounded color="primary" height="45" class="mt-12 font-weight-bold">Checkout</v-btn>
                </v-form>
              </v-stepper-content>
            </v-stepper-items>
          </v-stepper> -->

<v-stepper v-model="e1">
      <v-stepper-header>
        <v-stepper-step
          :complete="e1 > 1"
          step="1"
          color="info"
        >
          Kindly input your details
        </v-stepper-step>

        <v-divider></v-divider>

        <v-stepper-step
          :complete="e1 > 2"
          step="2"
          color="info"
        >
          Review your order
        </v-stepper-step>

        <v-divider></v-divider>

        <v-stepper-step color="info" step="3">
          Payment
        </v-stepper-step>
      </v-stepper-header>

      <v-stepper-items>
        <v-stepper-content step="1">
          <v-card
          elevation="0"
            class="mb-12"
            color=""
            height="500px"
          ></v-card>

          <v-btn
          depressed
            rounded
            color="secondary"
            @click="e1 = 2"
          >
            Continue
          </v-btn>


        </v-stepper-content>

        <v-stepper-content step="2">
          <v-card elevation="0"
            class="mb-12"
            color="grey lighten-1"
            height="500px"
          ></v-card>

          <v-btn
          depressed
            rounded
            color="secondary"
            @click="e1 = 3"
          >
            Continue
          </v-btn>

          <!-- <v-btn   @click="e1 = 2">
            Back
          </v-btn> -->
        </v-stepper-content>

        <v-stepper-content step="3">
          <v-card
            class="mb-12"
            color="grey lighten-1"
            height="500px"
          ></v-card>

          <v-btn
          depressed
            rounded
            color="secondary"
            @click="notificationDialog=true"
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
      <v-btn @click="notificationDialog=false" light icon class="close__btn white">
        <v-icon>mdi-close</v-icon>
      </v-btn>

      <div class="text-center px-5 pt-12 pb-7">
        <div class="title font-weight-bold mb-2">
          Congratulations there!
        </div>
        <div>
          <v-img src="/images/success-modal2.png" contain/>
        </div>
        <div class="info--text text--darken-2 font-weight-bold font__14">
          Kindly check your email your ticket.
        </div>
      </div>

      <div class="text-center px-5 pt-7 pb-12 primary">
        <div class="font-weight-bold white--text mb-5">
          Thank you for choosing tix.afica
        </div>
        <v-btn  width="150" to="/" depressed rounded color="white" class="black--text font-weight-bold font__12">View more events</v-btn>
      </div>
    </v-sheet>


  </v-dialog>
</main>
</template>

<script>

export default{
  layout : 'checkout',
  data(){
return{
  e1: 1,
  notificationDialog: false,
}
  }
}
</script>

<style lang="scss" scoped>
.bg {
  background: linear-gradient(0deg, rgb(3, 133, 149), rgba(255, 185, 81, 0.7)), url('/images/tix-reviews.png');
  height: 100vh;
  background-size: cover;
  background-position-x: 20%;

  @media screen and (max-width: 600px) {
    height: 0;
  }
}

.auth__title {
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
    background-color: #FC6436;

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
