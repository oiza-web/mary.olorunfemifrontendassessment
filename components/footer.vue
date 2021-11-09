<template>
<section class="bg">
    <v-container class="py-9">
        <v-row class="justify-space-between ">
            <v-col cols="12" lg="4">
                <img src="/images/quicklearn_white.png" height=""/>
                <div class="font-weight-light font__12 my-4">23, Kola Adeyina Close, <br> Off Admiralty Way, <br> Lekki, Lagos</div>

            </v-col>

            <v-col sm="12" lg="8" v-if="$vuetify.breakpoint.smAndUp">
                <div class="d-flex justify-space-between">

                <v-col cols="4" class="font-weight-thin font__12 ml-7" lg="3">
                    <div class="font-weight-bold font__16">Categories</div>
                    <div class="mt-1">Business Marketing</div>
                    <div class="mt-1">Web Development</div>
                    <div class="mt-1">UI design</div>
                    <div class="mt-1">Article Writing</div>
                    <div class="mt-1">Chinese Language</div>
                    <div class="mt-1">Marketing</div>
                    <div class="mt-1">Social Media Marketing</div>
                </v-col>

                <v-col cols="4" class="font-weight-light font__12" lg="3">
                    <div class="font-weight-bold font__16">Useful Links</div>
                    <div class="mt-1">Payment</div>
                    <div class="mt-1">Terms of Services</div>
                    <div class="mt-1">Your Account</div>
                    <div class="mt-1">Privacy</div>
                    <!-- <div class="mt-1">Contact us</div>
                    <div class="mt-1">Resume Maker</div> -->
                </v-col>

                <v-col md="2" :class="['font-weight-medium font__12', {'d-none': $vuetify.breakpoint.mdAndDown}]" lg="3">
                    <div class="font-weight-bold font__16">Support</div>
                    <div class="mt-1">FAQ</div>
                    <div class="mt-1">Contact Support</div>
                    <div class="mt-1">Call 0803 777 9999</div>
                    <div class="mt-1">Email support@quicklearn.com</div>
                    <div class="mt-3 font__16 font-weight-bold">Follow us on</div>
                    <!-- <div class="mt-1"></div> -->
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
      <!-- <hr class="hr"> -->
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
    background: #19005F;
    color: #FFFFFF;
}

</style>
