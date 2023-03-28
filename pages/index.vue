<template>
  <div>
    <v-row class="">
      <v-col cols="6">
        <lottie
          :width="700"
          :height="600"
          :options="lottieOptions"
          v-on:animCreated="handleAnimation"
        />
      </v-col>
      <v-col cols="6">
        <div class="titleText">
          <v-row class="fnt"> A </v-row>
          <v-row class="mt-2 fnt"> Business process change </v-row>
          <v-row class="fnt"> Type identifer Tool </v-row>
          <v-row class="fnt"> For smart cities. </v-row>
          <v-row class="mt-6">
            <v-btn class="btn-fnt" color="primary" outlined to="/requirements"> learn more </v-btn>
          </v-row>
        </div>
      </v-col>
    </v-row>

  </div>
</template>

<script>
import lottie from 'vue-lottie/src/lottie.vue'
import * as animationData from '~/assets/animation.json'
export default {
  components: {
    lottie,
  },
  data() {
    return {
      anim: null, // for saving the reference to the animation
      lottieOptions: { animationData: animationData.default },
    }
  },
  methods: {
    handleAnimation: function (anim) {
      this.anim = anim
    },
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Indie+Flower&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Urbanist:wght@500&display=swap');
.fp {
  height: 100vh;
}

.titleText {
  margin-top: 25%;
  margin-left: 20%;
}

.titleText-section2 {
  margin-top: 15%;
  margin-left: 20%;
}

.fnt {
  font-family: 'Urbanist', sans-serif;
  font-size: 30px;
  font-weight: bold;
}

.fnt-section2 {
  font-family: 'Urbanist', sans-serif;
  font-size: 20px;
}
.btn-fnt {
  font-family: 'Urbanist', sans-serif;
  font-size: 15px;
}

#section2 {
  height: 80vh;
  background-color: ghostwhite;
}

.section2-title {
  font-family: 'Urbanist', sans-serif;
  font-size: 40px;
  font-weight: bold;
}

.sectionM-title {
  font-family: 'Urbanist', sans-serif;
  font-size: 50px;
  font-weight: bold;
}
</style>
