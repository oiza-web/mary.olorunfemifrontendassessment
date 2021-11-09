<template>
    <section class="bg ">
      <v-container class="boxed__container pb-6">
          <div class="d-flex justify-center mt-4">
            <v-col lg="6">
                <div class="text-center font-weight-black primary--text font__40 my-4">Upcoming Events</div>

            </v-col>
        </div>
          <v-row class="mx-8">
            <v-col cols="12" lg="3" md="6" sm="12">
            <v-hover v-slot="{ hover }">
                <v-card height="400" color="white" elevation="0">
                <v-img src="/images/event1.jpg" height="60%"></v-img>
                <v-card-text class="primary--text font__12 font-weight-bold">Jhonny Drille live</v-card-text>
                <div class="font__15 mx-4 font-weight-black primary--text">Christmas concert</div>
                <v-expand-transition>
                  <div v-if="hover" class="darken-2 v-card--reveal text-h2 white--text"><v-btn to="/checkout" class="mt-2 mx-4 white--text caption font-weight-bold" width="200px"  rounded elevation="0" color="primary">Register</v-btn></div>
                </v-expand-transition>
                <div v-if="!hover" class="d-flex  font__10 mx-4 my-6 justify-space-between primary--text font-weight-medium"><p>20 Tickets left</p>
                <p>2days to go</p>

                </div>
              </v-card>
            </v-hover>
            </v-col>
            <v-col cols="12" lg="3" md="6" sm="12">
              <v-hover v-slot="{ hover }">
                <v-card height="400px" elevation="0"><v-img src="/images/event1.jpg" height="60%"></v-img>
                  <v-card-text class="primary--text font__12 font-weight-bold">Jhonny Drille live </v-card-text>
                    <div class="font__15 mx-4 font-weight-black primary--text">Christmas concert</div>
                    <v-expand-transition>
                  <div v-if="hover" class="darken-2 v-card--reveal text-h2 white--text"><v-btn to="/checkout" class="mt-2 white--text  mx-4 caption font-weight-bold" width="200px"  rounded elevation="0" color="primary">Register</v-btn></div>
                  </v-expand-transition>
                    <div v-if="!hover" class="d-flex  font__10 mx-4 my-6 justify-space-between primary--text font-weight-medium"><p>20 Tickets left</p>
                <p>2days to go</p>

                </div>
              </v-card>
              </v-hover>
            </v-col>
            <v-col cols="12" lg="3" md="6" sm="12">
              <v-hover v-slot="{ hover }">
                <v-card height="400px" elevation="0"><v-img src="/images/event1.jpg"  height="250"></v-img>
                <v-card-text class="primary--text font__12 font-weight-bold">Jhonny Drille live </v-card-text>
                <div class="font__15 mx-4 font-weight-black primary--text">Christmas concert</div>
                <v-expand-transition>
                  <div v-if="hover" class="darken-2 v-card--reveal text-h2 white--text"><v-btn to="/checkout" class="mt-2 white--text mx-4 caption font-weight-bold" width="200px"  rounded elevation="0" color="primary">Register</v-btn></div>
                  </v-expand-transition>
               <div v-if="!hover" class="d-flex  font__10 mx-4 my-6 justify-space-between primary--text font-weight-medium"><p>20 Tickets left</p>
                <p>2days to go</p>

                </div>
              </v-card>
              </v-hover>
            </v-col>
            <v-col cols="12" lg="3" md="6" sm="12">
              <v-hover v-slot="{ hover }">
                <v-card height="400px" elevation="0"><v-img src="/images/event1.jpg" height="60%"></v-img>
                <v-card-text class="primary--text font__12 font-weight-bold">Jhonny Drille live </v-card-text>
                <div class="font__15 mx-4 font-weight-black primary--text">Christmas concert</div>
                <v-expand-transition>
                  <div v-if="hover" class="darken-2 v-card--reveal text-h2 primary--text "><v-btn to="/checkout" class="mt-2 white--text caption mx-4 font-weight-bold" width="200px"  rounded elevation="0" color="primary">Register</v-btn></div>
                  </v-expand-transition>
                <div v-if="!hover" class="d-flex  font__10 mx-4 my-6 justify-space-between primary--text font-weight-medium"><p>20 Tickets left</p>
                <p>2days to go</p>

                </div>
              </v-card>
              </v-hover>
            </v-col>
          </v-row>
          </v-container>
    </section>
</template>
<style lang="scss" scoped>
.bg{
  background-color:#D0F7FC;
}
</style>
