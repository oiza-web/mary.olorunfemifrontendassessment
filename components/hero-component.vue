<template>
  <v-container fill-height fluid class="bg">
    <section class="boxed__container">
      <v-row :class="[$vuetify.breakpoint.mdAndUp ? 'mt-15' : 'mt-0', $vuetify.breakpoint.mdAndUp ? 'justify-space-between': 'justify-center', 'my-auto']">
            <v-col cols="12" md="6" lg="5" class="mx-auto my-13">

                <div class="hero font-weight-extra-bold primary--text font__70">
                  <p class="font__40 secondary--text font-weight-light emphasize mt-10">your e learning partner</p>
                    Online  Learning, <br> But in Bitesize
                </div>

                <div class="my-6 primary--text font-weight-medium font__16 mt-10">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Rem ex esse ullam libero, nostrum dolorem nam error expedita nemo, vitae nisi natus ab tempore in omnis reiciendis enim.
                </div>

                <div :class="[{'mt-9': $vuetify.breakpoint.xsOnly}]">
                    <v-btn exact to="#" :loading="loading" depressed rounded class="text-capitalize btn font__12 primary--text caption mt-10" :width="$vuetify.breakpoint.xsOnly ? '100%' : '150'" height="50" color="cta">Try Now</v-btn>
                    <!-- <v-btn nuxt exact to="#" depressed rounded :class="[$vuetify.breakpoint.xsOnly ? 'ml-0 mt-10' :'ml-8', 'text-capitalize font__12 font-weight-bold']" style="color:black !important;" outlined :width="$vuetify.breakpoint.xsOnly ? '100%' : '150'" color="primary">Play Video</v-btn> -->
                    <!-- <img src="/images/play_video.png" height="50px" width="50px" class="mt-auto"/> Play Now -->
                </div>
            </v-col>
            <v-col md="6" :class="[{'d-none': $vuetify.breakpoint.smAndDown }]" lg="6">
                <v-img loading="lazy" height="950" contain src="/images/hero-image-tix.png" />
            </v-col>
        </v-row>
    </section>
  </v-container>
</template>
<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Aguafina+Script&family=Allura&display=swap');
.bg {
    background: url('/images/bg.png');
    background-size: cover;
    background-repeat: no;
    // background-position-x: -7.5rem;
    // background-position-y: -3.5rem;
    // min-height: 70vh;

    @media (max-width: 1024px) {
        min-height: 100%;
        background-position-x: 59%;
        background-position-y: 24%;

    }

    @media (max-width: 768px) {
        background-position-y: 76% !important;
        background: url('/images/bg-hero.png');

    }

    @media (min-width: 1700px) {
        background-position-x: 22.5rem;

    }
}

.hero__heading {
    font-size: 3rem;
    font-weight: 800;
    margin-top: 8rem;

    @media (max-width: 1024px) {
        font-size: 2rem;

    }

    @media (max-width: 425px) {
        font-size: 1.4rem;
        margin-top: 5rem;

    }
}

.btn {
    font-weight: 600;
}

.flexIt-goal {
    width: 80%;

    @media (max-width: 425px) {
        width: 100%;

    }
}

.brand-focus-text {
    width: 40%;

    @media (max-width: 1024px) {
        width: 60% !important;
    }

    @media (max-width: 425px) {
        width: 100% !important;
    }

}

.brand-title {
    font-weight: 800;
}
</style>
