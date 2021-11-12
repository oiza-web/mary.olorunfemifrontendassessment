<template>
<section class="bg">
    <v-container class="py-9">
        <v-row class="justify-space-between ">
            <v-col cols="12" lg="4">
                <img src="/images/tix-logo-white.png" height="40"/>
                <div class="font-weight-light font__12 my-4">23, Kola Adeyina Close, <br> Off Admiralty Way, <br> Lekki, Lagos</div>

            </v-col>

            <v-col sm="12" lg="8" v-if="$vuetify.breakpoint.smAndUp">
                <div class="d-flex justify-space-between">

                <v-col cols="4" class="font-weight-thin font__12 ml-7" lg="3">
                    <div class="font-weight-bold font__16">Categories</div>
                    <div class="mt-1">Events</div>
                    <div class="mt-1">Products</div>
                    <div class="mt-1">Pricing</div>
                    <div class="mt-1">Blog</div>
                    <div class="mt-1">Marketing</div>

                </v-col>

                <v-col cols="4" class="font-weight-light font__12" lg="3">
                    <div class="font-weight-bold font__16">Useful Links</div>
                    <div class="mt-1">Payment</div>
                    <div class="mt-1">Terms of Services</div>
                    <div class="mt-1">Your Account</div>
                    <div class="mt-1">Privacy</div>

                </v-col>

                <v-col md="2" :class="['font-weight-medium font__12', {'d-none': $vuetify.breakpoint.mdAndDown}]" lg="3">
                    <div class="font-weight-bold font__16">Support</div>
                    <div class="mt-1">FAQ</div>
                    <div class="mt-1">Contact Support</div>
                    <div class="mt-1">Call 0803 777 9999</div>
                    <div class="mt-1">Email support@tix.africa.com</div>
                    <div class="mt-3 font__16 font-weight-bold">Follow us on</div>

                    <div class="mt-2">
                      <v-icon color="white" size="18" class="ml-2">mdi-facebook</v-icon>
                      <v-icon color="white" size="18" class="ml-2">mdi-linkedin</v-icon>
                      <v-icon color="white" size="18" class="ml-2">mdi-twitter</v-icon>
                      <v-icon color="white" size="18" class="ml-2">mdi-instagram </v-icon>
                    </div>
                </v-col>
                </div>
            </v-col>
        </v-row>
      
      <v-divider></v-divider>
    </v-container>
</section>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.bg {
    background: black;
    color: #FFFFFF;
}

</style>
