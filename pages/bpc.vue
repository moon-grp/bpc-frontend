<template>
  <div>
    <v-row class="sectionM-title my-5" justify="center">
      <div>Business process change</div>
    </v-row>
    <v-row class="ml-0 mt-6" id="section1">
      <v-col cols="6">
        <div class="titleText-section2">
          <v-row class="mt-8 mr-5 fnt-section2">
            Business process change refers to the practice of making significant
            alterations to the way a company operates in order to improve
            efficiency, reduce costs, increase customer satisfaction, or achieve
            other desired outcomes. This can involve changes to workflows,
            procedures, technologies, organizational structures, and other
            aspects of the business.
          </v-row>
        </div>
      </v-col>
      <v-col cols="6">
        <div class="mt-6">
          <v-img src="https://res.cloudinary.com/sparaclet-inc/image/upload/v1680217877/sparaclet%20inc/BPC3_igasik.jpg" height="300" width="600" contain></v-img>
        </div>
      </v-col>
    </v-row>
    <v-row class="sectionM-title my-5" justify="center">
      <div>Why business process change?</div>
    </v-row>
    <v-row class="ml-4 mt-4" id="section2">
      <v-col cols="5">
        <div class="mt-6 ml-5">
          <v-img src="https://res.cloudinary.com/sparaclet-inc/image/upload/v1680217876/sparaclet%20inc/Benefits__w3me9x.png" height="500" width="600" contain></v-img>
        </div>
      </v-col>

      <v-col cols="6">
        <div class="titleText-section2">
          <v-row class="mt-2 fnt-section2">
            Business process change is the practice of making significant
            alterations to the way a company operates in order to improve
            efficiency, reduce costs, increase customer satisfaction, or achieve
            other desired outcomes. It involves changes to workflows,
            procedures, technologies, organizational structures, and other
            aspects of the business. This practice is necessary to adapt to
            changing market conditions, regulatory requirements, and advances in
            technology. By streamlining operations, enhancing quality, reducing
            costs, responding to market demands, and adopting new technologies,
            businesses can remain competitive and meet the needs of their
            customers while increasing profitability. Effective business process
            change requires careful planning, communication, and management to
            ensure that changes are implemented smoothly and with minimal impact
            on the business.
          </v-row>
        </div>
      </v-col>
    </v-row>
    <v-row class="sectionM-title my-5" justify="center">
      <div>What are business process change type identifier</div>
    </v-row>
    <v-row class="ml-0 mt-6" id="section3">
      <v-col cols="6">
        <div class="titleText-section2">
          <v-row class="mt-4 mr-5 fnt-section2">
            There are six types of business process change: incremental change,
            radical change, business process reengineering (BPR), continuous
            improvement, process automation, and process standardization.
            Incremental change involves small improvements, while radical change
            involves a complete overhaul. BPR involves rethinking the entire
            process. Continuous improvement involves ongoing improvements.
            Process automation uses technology, and process standardization
            establishes consistent processes.
          </v-row>
        </div>
      </v-col>
      <v-col cols="6">
        <div class="mt-5">
          <v-img src="https://res.cloudinary.com/sparaclet-inc/image/upload/v1680217875/sparaclet%20inc/Cen__gwb0gt.png" height="300" width="600" contain></v-img>
        </div>
      </v-col>
    </v-row>

    <v-row class="sectionM-title my-5" justify="center">
      <div>Why BPC type identifier is neccessary</div>
    </v-row>
    <v-row class="mt-6" id="section1">
      <v-row class="mt-4 mx-8 fnt-section2">
        There are six types of business process change: incremental change, The
        importance of business process change type identifier lies in the fact
        that different types of changes require different approaches,
        strategies, and resources to be successful. <br />
        By identifying the appropriate type of change needed, organizations can
        more effectively plan, implement, and manage the change process. For
        example, incremental changes may be suitable for situations where the
        process only needs minor improvements, while radical changes may be
        necessary when the existing process is no longer effective or relevant.
        <br />
        Process reengineering may be needed for significant performance
        improvements, while process automation can be effective for streamlining
        repetitive tasks. By understanding the different types of change,
        organizations can choose the most appropriate approach to meet their
        specific goals and improve overall performance.
      </v-row>
      <v-row class="my-8" justify="center">
        <v-btn class="btn-fnt text-capitalize" color="primary" outlined to="/typid">
          click to use business process change type identifier tool
        </v-btn>
      </v-row>
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
  margin-top: 5%;
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

#section1 {
  height: 70vh;
  background-color: ghostwhite;
}

#section2 {
  height: 100vh;
  background-color: ghostwhite;
}

#section3 {
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
