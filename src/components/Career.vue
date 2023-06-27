<template>
  <div id="career" class="py-5">
    <h1 class="text-center mb-5">Career Timeline</h1>
    <vue-slider v-model="value" :marks="marks" :tooltip="'always'" :process="false"></vue-slider>
  </div>
</template>

<script>
import VueSlider from 'vue-slider-component'
import 'vue-slider-component/theme/default.css'

export default {

  name: 'CareerSection',
  components: {
    VueSlider,
  },
  data() {
    return {
      value: [2],
      marks: {
        1: 'Start Career',
        2: 'First Job',
        3: 'Promotion',
        4: 'Current Role'
      }
    }
  }
}
</script>
