<template>
  <section>
 <herocomponent/>
 <golive />
 <events />
 <reviews/>
  </section>
</template>

<script>
import herocomponent from '../components/landingpage/hero-component.vue'
import golive from '../components/landingpage/golive.vue'
import events from '../components/landingpage/events.vue'
import reviews from '../components/landingpage/reviews.vue'

export default {
  components :{
    herocomponent, golive, events, reviews
  }

}
</script>
