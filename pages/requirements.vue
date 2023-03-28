<template>
  <div>
    <v-row class="sectionM-title my-5" justify="center">
      <div>What are smart cities?</div>
    </v-row>
    <v-row class="ml-0 mt-6" id="section2">
      <v-col cols="6">
        <div class="titleText-section2">
          <v-row class="mt-2 mr-5 fnt-section2">
            Smart cities are urban areas that use advanced technology and data
            analytics to improve the quality of life for residents, enhance
            sustainability, and streamline urban services. These cities use a
            variety of Internet of Things (IoT) devices, sensors, and data
            analytics tools to collect and analyze information about everything
            from traffic patterns and energy consumption to air quality and
            waste management.
          </v-row>
        </div>
      </v-col>
      <v-col cols="6">
        <div class="mt-8">
          <v-img src="/smart_.png" height="300" width="600"></v-img>
        </div>
      </v-col>
    </v-row>
    <v-row class="sectionM-title my-5" justify="center">
      <div>Requirements of smart cities?</div>
    </v-row>
    <v-row class="ml-0 mt-6" id="section3">
      <v-col cols="5">
        <div class="mt-6 ml-4">
          <v-img src="/req-1.png" height="500" width="650"></v-img>
        </div>
      </v-col>

      <v-col cols="6">
        <div class="titleText-section2">
          <v-row class="mt-4 fnt-section2">
            To become a smart city, robust digital infrastructure and Internet
            of Things (IoT) devices are required. Smart cities use advanced
            technology and data analytics to improve the quality of life for
            residents, enhance sustainability, and streamline urban services.
            They use IoT devices, sensors, and data analytics tools to collect
            and analyze information about everything from traffic patterns and
            energy consumption to air quality and waste management. Smart cities
            aim to optimize the use of resources, reduce waste, and enhance the
            overall efficiency of urban systems. By using technology to improve
            the delivery of services and provide real-time information to
            residents, smart cities aim to create a more livable and sustainable
            environment for all.
          </v-row>
        </div>
      </v-col>
    </v-row>
    <v-row class="sectionM-title my-5" justify="center">
      <div>System integration For smart cities</div>
    </v-row>
    <v-row class="ml-0 mt-6" id="section3">
      <v-col cols="6">
        <div class="titleText-section2">
          <v-row class="mt-4 mr-5 fnt-section2">
            System integration is a crucial aspect of building a smart city. It
            involves the integration of various systems, including data
            management systems, communication networks, transportation systems,
            and energy management systems. The integration of these systems
            enables smart cities to function efficiently and deliver better
            services to their residents. To achieve system integration in a
            smart city, it is important to establish a common platform that
            connects all systems and devices. This platform should be able to
            gather and analyze data from various sources, and provide insights
            that can be used to improve urban services. Additionally, open data
            standards and protocols should be established to enable seamless
            communication between different systems.
          </v-row>
        </div>
      </v-col>
      <v-col cols="6">
        <div class="mt-5">
          <v-img src="/system_.jpg" height="500" width="600"></v-img>
        </div>
      </v-col>
    </v-row>
    <v-row class="my-8" justify="center">
      <v-btn class="btn-fnt"  color="primary" outlined to="/bpc">
        learn more
      </v-btn>
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

#section3 {
  height: 100vh;
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
