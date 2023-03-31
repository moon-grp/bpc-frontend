<template>
  <div>
    <v-card class="mx-auto mt-14" max-width="600">
      <v-card-title class="text-h6 font-weight-regular justify-space-between">
        <span>{{ currentTitle }}</span>
        <v-avatar
          color="primary"
          class="subheading white--text caption"
          size="24"
          v-text="step"
        ></v-avatar>
      </v-card-title>

      <v-window v-model="step">
        <v-window-item :value="1">
          <v-card-text>
            <span class="text-caption grey--text text--darken-1">
              Is the targeted process merely tagnetial <b>or</b> integral to the
              city's strategic goals and objectives.
            </span>
            <div class="pt-4 text-caption grey--text text--darken-1">
              (1) <b>Strongly disagree</b> <span class="space"></span>(5)
              <b>Strongly agree</b>
            </div>
            <v-radio-group v-model="strategicCentrality" row>
              <v-radio label="1" value="1"></v-radio>
              <v-radio label="2" value="2"></v-radio>
              <v-radio label="3" value="3"></v-radio>
              <v-radio label="4" value="4"></v-radio>
              <v-radio label="5" value="5"></v-radio>
            </v-radio-group>
          </v-card-text>
        </v-window-item>

        <v-window-item :value="2">
          <v-card-text>
            <span class="text-caption grey--text text--darken-1">
              Does IT enable only incidental change <b>or</b> fundamental
              process change to the project
            </span>
            <div class="pt-4 text-caption grey--text text--darken-1">
              (1) <b>Strongly disagree</b> <span class="space"></span>(5)
              <b>Strongly agree</b>
            </div>
            <v-radio-group v-model="feasibiltyOfIt" row>
              <v-radio label="1" value="1"></v-radio>
              <v-radio label="2" value="2"></v-radio>
              <v-radio label="3" value="3"></v-radio>
              <v-radio label="4" value="4"></v-radio>
              <v-radio label="5" value="5"></v-radio>
            </v-radio-group>
          </v-card-text>
        </v-window-item>

        <v-window-item :value="3">
          <v-card-text>
            <span class="text-caption grey--text text--darken-1">
              Is the scope of the process intra-functional (limited to a specific area) <b>or</b>
              interorganization (not limited to a specific area)
            </span>
            <div class="pt-4 text-caption grey--text text--darken-1">
              (1) <b>Strongly disagree</b> <span class="space"></span>(5)
              <b>Strongly agree</b>
            </div>
            <v-radio-group v-model="processBreadth" row>
              <v-radio label="1" value="1"></v-radio>
              <v-radio label="2" value="2"></v-radio>
              <v-radio label="3" value="3"></v-radio>
              <v-radio label="4" value="4"></v-radio>
              <v-radio label="5" value="5"></v-radio>
            </v-radio-group>
          </v-card-text>
        </v-window-item>

        <v-window-item :value="4">
          <v-card-text>
            <span class="text-caption grey--text text--darken-1">
              Is the senior management visibly removed in the BPR efforts <b>or</b> actively
              involved in the BPR efforts.
            </span>
            <div class="pt-4 text-caption grey--text text--darken-1">
              (1) <b>Strongly disagree</b> <span class="space"></span>(5)
              <b>Strongly agree</b>
            </div>
            <v-radio-group v-model="seniorManagementCommitment" row>
              <v-radio label="1" value="1"></v-radio>
              <v-radio label="2" value="2"></v-radio>
              <v-radio label="3" value="3"></v-radio>
              <v-radio label="4" value="4"></v-radio>
              <v-radio label="5" value="5"></v-radio>
            </v-radio-group>
          </v-card-text>
        </v-window-item>

        <v-window-item :value="5">
          <v-card-text>
            <span class="text-caption grey--text text--darken-1">
              Are preferred performance measurement critieria efficency based
              <b>or</b> Effectiveness based
            </span>
            <div class="pt-4 text-caption grey--text text--darken-1">
              (1) <b>Strongly disagree</b> <span class="space"></span>(5)
              <b>Strongly agree</b>
            </div>
            <v-radio-group v-model="perfomanceManagement" row>
              <v-radio label="1" value="1"></v-radio>
              <v-radio label="2" value="2"></v-radio>
              <v-radio label="3" value="3"></v-radio>
              <v-radio label="4" value="4"></v-radio>
              <v-radio label="5" value="5"></v-radio>
            </v-radio-group>
          </v-card-text>
        </v-window-item>

        <v-window-item :value="6">
          <v-card-text>
            <span class="text-caption grey--text text--darken-1">
            (the ability of a process to perform steps or actions effectively and efficiently, resulting in successful outcomes)<br>
            </span>
            <span class="text-caption grey--text text--darken-1">
              Is the process fucntioning marginally <b>or</b> is the process not
              functioning well at all
            </span>
            <div class="pt-4 text-caption grey--text text--darken-1">
              (1) <b>Strongly disagree</b> <span class="space"></span>(5)
              <b>Strongly agree</b>
            </div>
            <v-radio-group v-model="processFunctionality" row>
              <v-radio label="1" value="1"></v-radio>
              <v-radio label="2" value="2"></v-radio>
              <v-radio label="3" value="3"></v-radio>
              <v-radio label="4" value="4"></v-radio>
              <v-radio label="5" value="5"></v-radio>
            </v-radio-group>
          </v-card-text>
        </v-window-item>

        <v-window-item :value="7">
          <v-card-text>
            <span class="text-caption grey--text text--darken-1">
              Are only minimal resources availble to support the
              process change <b>or</b> are resources abundant ?
            </span>
            <div class="pt-4 text-caption grey--text text--darken-1">
              (1) <b>Strongly disagree</b> <span class="space"></span>(5)
              <b>Strongly agree</b>
            </div>
            <v-radio-group v-model="processResource" row>
              <v-radio label="1" value="1"></v-radio>
              <v-radio label="2" value="2"></v-radio>
              <v-radio label="3" value="3"></v-radio>
              <v-radio label="4" value="4"></v-radio>
              <v-radio label="5" value="5"></v-radio>
            </v-radio-group>
          </v-card-text>
        </v-window-item>

        <v-window-item :value="8">
          <v-card-text>
            <span class="text-caption grey--text text--darken-1">
              Is the organizational structure rigid <b>or</b> it is flexibly
              conducive to change and learning?
            </span>
            <div class="pt-4 text-caption grey--text text--darken-1">
              (1) <b>Strongly disagree</b> <span class="space"></span>(5)
              <b>Strongly agree</b>
            </div>
            <v-radio-group v-model="structureFeasibility" row>
              <v-radio label="1" value="1"></v-radio>
              <v-radio label="2" value="2"></v-radio>
              <v-radio label="3" value="3"></v-radio>
              <v-radio label="4" value="4"></v-radio>
              <v-radio label="5" value="5"></v-radio>
            </v-radio-group>
          </v-card-text>
        </v-window-item>

        <v-window-item :value="9">
          <v-card-text>
            <span class="text-caption grey--text text--darken-1">
              Does the culture support the status quo <b>or</b> actively seek
              particptory change?
            </span>
            <div class="pt-4 text-caption grey--text text--darken-1">
              (1) <b>Strongly disagree</b> <span class="space"></span>(5)
              <b>Strongly agree</b>
            </div>
            <v-radio-group v-model="culturalCapacity" row>
              <v-radio label="1" value="1"></v-radio>
              <v-radio label="2" value="2"></v-radio>
              <v-radio label="3" value="3"></v-radio>
              <v-radio label="4" value="4"></v-radio>
              <v-radio label="5" value="5"></v-radio>
            </v-radio-group>
          </v-card-text>
        </v-window-item>

        <v-window-item :value="10">
          <v-card-text>
            <span class="text-caption grey--text text--darken-1">
              Are only modest impacts on the people tolerable <b>or</b> is
              management willing to deal with the consquences of disruptive
              impacts
            </span>
            <div class="pt-4 text-caption grey--text text--darken-1">
              (1) <b>Strongly disagree</b> <span class="space"></span>(5)
              <b>Strongly agree</b>
            </div>
            <v-radio-group v-model="managementWillingness" row>
              <v-radio label="1" value="1"></v-radio>
              <v-radio label="2" value="2"></v-radio>
              <v-radio label="3" value="3"></v-radio>
              <v-radio label="4" value="4"></v-radio>
              <v-radio label="5" value="5"></v-radio>
            </v-radio-group>
          </v-card-text>
        </v-window-item>

        <v-window-item :value="11">
          <v-card-text>
            <span class="text-caption grey--text text--darken-1">
              Is the BPR effort targeted at an internal support process
              <b>or</b> a core process
            </span>
            <div class="pt-4 text-caption grey--text text--darken-1">
              (1) <b>Strongly disagree</b> <span class="space"></span>(5)
              <b>Strongly agree</b>
            </div>
            <v-radio-group v-model="valueChain" row>
              <v-radio label="1" value="1"></v-radio>
              <v-radio label="2" value="2"></v-radio>
              <v-radio label="3" value="3"></v-radio>
              <v-radio label="4" value="4"></v-radio>
              <v-radio label="5" value="5"></v-radio>
            </v-radio-group>
          </v-card-text>
        </v-window-item>

        <v-window-item :value="12">
          <v-card-text>
            <span class="text-caption grey--text text--darken-1">
              Risk propensity of the decision makers.
            </span>
            <div class="pt-4 text-caption grey--text text--darken-1">
              (1) <b>risk averse</b> <span class="space"></span>(5)
              <b>risk taking</b>
            </div>
            <v-radio-group v-model="riskPropensity" row>
              <v-radio label="1" value="1"></v-radio>
              <v-radio label="2" value="2"></v-radio>
              <v-radio label="3" value="3"></v-radio>
              <v-radio label="4" value="4"></v-radio>
              <v-radio label="5" value="5"></v-radio>
            </v-radio-group>
          </v-card-text>
        </v-window-item>
      </v-window>

      <v-divider></v-divider>

      <v-card-actions>
        <v-btn :disabled="step === 1" text @click="step--"> Back </v-btn>
        <v-spacer></v-spacer>
        <v-btn
          :disabled="step === 12"
          color="primary"
          depressed
          @click="step++"
          outlined
          class="text-capitalize"
        >
          Next
        </v-btn>
        <v-btn
          @click="getRes"
          class="text-capitalize"
          color="primary"
          outlined
          :disabled="step !== 12"
        >
          Indentify Change type</v-btn
        >
      </v-card-actions>
    </v-card>
    <v-snackbar v-model="snackbar" :timeout="timeout" color="success" top>
      {{ msg }}
    </v-snackbar>
    <v-snackbar v-model="snackbarErr" :timeout="timeout" color="red" top>
      {{ msg }}
    </v-snackbar>

    <v-dialog v-model="dialog1" width="600px" fullscreen>
      <v-card>
        <v-toolbar dark color="primary">
          <v-btn icon dark @click="dialog1 = false">
            <v-icon>mdi-close</v-icon>
          </v-btn>
        </v-toolbar>
        <v-card-title>
          <span class="headline">Evolutionary Approach should be used</span>
        </v-card-title>
        <v-card-text>
          This approach focuses on gradual and continuous improvements to
          business processes. This approach is designed to help cities
          achieve better results without causing significant disruptions to
          their daily operations. By implementing this approach, cities can
          better adapt to changing circumstances and improve their efficiency
          and effectiveness over time.
        </v-card-text>
        <v-card-title>
          <span class="headline">Example</span>
        </v-card-title>
        <v-card-text>
          <div class="mb-4">
            <span class="caption">
              When considering changes to a particular process, such as the way
              they collect and dispose of waste in a city, the evolutionary
              approach would be to make small, incremental changes to the
              process to see how it affects the overall outcome. <br />
              This approach is useful because it allows the city to test out
              changes on a smaller scale, without committing to a large,
              expensive overhaul of the entire process. By making small changes
              and measuring their impact, the city can identify areas for
              improvement and refine the process over time. <br />
              Evolutionary approach can help the city be more responsive to
              changing circumstances. If a new development project is announced,
              for example, the city can use the evolutionary approach to make
              small changes to the permitting process to ensure that it remains
              efficient and effective even as demand for permits increases.
            </span>
          </div>

          <div>
            <span class="caption">
              <b>The Evolutionary</b> approach to business process change can be
              a valuable tool for city administrators because it allows them to
              make data-driven decisions based on small, incremental changes. By
              using this approach, city admin can make informed decisions that
              are tailored to the city's specific needs and circumstances,
              rather than relying on one-size-fits-all solutions. This can help
              them to better serve their constituents and achieve their goals.
            </span>
          </div>
        </v-card-text>
      </v-card>
    </v-dialog>

    <v-dialog v-model="dialog2" width="600px" fullscreen>
      <v-card>
        <v-toolbar dark color="primary">
          <v-btn icon dark @click="dialog2 = false">
            <v-icon>mdi-close</v-icon>
          </v-btn>
        </v-toolbar>
        <v-card-title>
          <span class="headline">Revolutionary Approach should be used</span>
        </v-card-title>
        <v-card-text>
          This approach to business process change emphasizes large-scale
          changes to business processes in a relatively short period of time.
          This approach is designed to address major inefficiencies or problems
          in a business's operations, and can be particularly useful in
          situations where incremental improvements are not sufficient.
        </v-card-text>
        <v-card-title>
          <span class="headline">Example</span>
        </v-card-title>
        <v-card-text>
          <div class="">
            <span class="caption">
              If a city has identified a major issue with the way that they are
              collecting and disposing of waste, a revolutionary approach could
              involve a complete overhaul of the entire process, with the aim of
              creating a more efficient and effective system. <br />

              For areas such as reducing traffic congestion or improving public
              transportation, a revolutionary approach could involve making
              large-scale changes to the transportation infrastructure or
              introducing new policies and regulations to achieve these goals.
              <br />

              The revolutionary approach can also help the city to stay
              competitive and innovative in a rapidly changing environment. By
              being willing to take bold and decisive action, the city can stay
              ahead of the curve and respond to emerging trends and challenges
              more effectively.
            </span>
          </div>
        </v-card-text>

        <v-card-title class="headline">Conclusion</v-card-title>
        <v-card-text>
          <span class="caption">
            The revolutionary approach to business process change can be
            beneficial to a city in several ways. It can help the council to
            address major issues or problems in its operations, achieve its
            goals more quickly, and stay competitive and innovative in a rapidly
            changing environment.
          </span>
        </v-card-text>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
export default {
  layout: 'tpid',
  data: () => ({
    msg: '',
    snackbarErr: '',
    snackbar: false,
    timeout: 9000,
    step: 1,
    strategicCentrality: '',
    feasibiltyOfIt: '',
    processBreadth: '',
    seniorManagementCommitment: '',
    perfomanceManagement: '',
    processFunctionality: '',
    processResource: '',
    structureFeasibility: '',
    culturalCapacity: '',
    managementWillingness: '',
    valueChain: '',
    riskPropensity: '',
    ticksLabels: ['Figs', 'Lemon', 'Pear', 'Apple'],
    dialog1: false,
    dialog2: false,
  }),

  computed: {
    currentTitle() {
      switch (this.step) {
        case 1:
          return 'Strategic Centrality of the project'
        case 2:
          return 'Feasibility of IT to change the project'
        case 3:
          return 'Process breadth'
        case 4:
          return 'Senior management commitment'
        case 5:
          return 'Performace management criteria'
        case 6:
          return 'Process functionality'
        case 7:
          return 'Process resource availabilty'
        case 8:
          return 'Structural feasibilty'
        case 9:
          return 'Cultural capacity for change'
        case 10:
          return 'Management willingness to impact people'
        case 11:
          return 'Value chain target'
        case 12:
          return 'Risk propensity'
        default:
          return 'Account created'
      }
    },
  },
  methods: {
    async getRes() {
      try {
        const res = await this.$axios.post(
          'https://sea-turtle-app-ostth.ondigitalocean.app/bpc/',
          {
            strategicCentrality: parseInt(this.strategicCentrality),
            feasibiltyOfIt: parseInt(this.feasibiltyOfIt),
            processBreadth: parseInt(this.processBreadth),
            seniorManagementCommitment: parseInt(
              this.seniorManagementCommitment
            ),
            perfomanceManagement: parseInt(this.perfomanceManagement),
            processFunctionality: parseInt(this.processFunctionality),
            processResource: parseInt(this.processResource),
            structureFeasibility: parseInt(this.structureFeasibility),
            culturalCapacity: parseInt(this.culturalCapacity),
            managementWillingness: parseInt(this.managementWillingness),
            riskPropensity: parseInt(this.riskPropensity),
            valueChain: parseInt(this.valueChain),
          }
        )

        if (res.data.BPC == 'evolutionary') {
          this.dialog2 = false
          this.dialog1 = true
        }
        if (res.data.BPC == 'revolutionary') {
          this.dialog1 = false
          this.dialog2 = true
        }
      } catch (error) {
        console.log(error)
        this.msg = 'error occured: kindly tick all buttons'
        this.snackbarErr = true
      }
    },
  },
}
</script>

<style>
.space {
  margin-left: 10px;
}
</style>
