<template>
  <v-layout row justify-center align-center wrap class="mt-4 pt-2">
    <v-flex xs12 sm12 md5 lg6 xl6 class="mt-4 pt-4">
      <h2 class="mb-4 pl-4 pt-2">Education</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>
          <v-timeline-item color="light-blue darken-4" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold light-blue--text text--darken-4">2009</div>
                <div class="caption font-weight-bold light-blue--text text--darken-4">2013</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Art college of the republic of Uzbekistan</strong>
                <div class="caption mb-2">Faculty of Graphics</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="light-blue darken-4" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold light-blue--text text--darken-4">2014</div>
                <div class="caption font-weight-bold light-blue--text text--darken-4">2015</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>12 principles of animation courses</strong>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="light-blue darken-4" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold light-blue--text text--darken-4">2021</div>
                <div class="caption font-weight-bold light-blue--text text--darken-4">Present</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Frontend developing courses</strong>
              </v-flex>
            </v-layout>
          </v-timeline-item>
        </v-timeline>
      </v-card-text>
    </v-flex>
    <v-flex xs12 sm12 md4 lg6 xl6 class="mt-4 pt-2">
      <h2 class="mb-4 pl-4">Experience</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>
          <v-timeline-item color="light-blue darken-4" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold light-blue--text text--darken-4">2009</div>
                <div class="caption font-weight-bold light-blue--text text--darken-4">2015</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Cinema.uz (Tashkent, Uzbekistan)</strong>
                <div class="caption mb-2">
                  3D Animator and 3D Modeller
                  <br>
                  Short film, Advertisments
                  <br>
                  Modelling for CNC router
                </div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="light-blue darken-4" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold light-blue--text text--darken-4">2016</div>
                <div class="caption font-weight-bold light-blue--text text--darken-4">2017</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Freelance (Istanbul, Turkey)</strong>
                <div class="caption mb-2">3D Animator and 3D Modeller</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

        </v-timeline>
      </v-card-text>
    </v-flex>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-flex xs12 sm12 md4 lg5 xl5 class="mx-2 pt-4">
        <h2>
          <span>Design</span>

          <span class="light-blue--text text--darken-4">Skills</span>
        </h2>
        <br>
        <strong>3D modeling</strong>
        <v-progress-linear v-model="buffer1" :buffer-value="bufferValue" color="light-blue darken-4" height="16"></v-progress-linear>
        <strong>Animating</strong>
        <v-progress-linear v-model="buffer2" :buffer-value="bufferValue" color="light-blue darken-4" height="16"></v-progress-linear>
        <strong>Texturing & Rigging</strong>
        <v-progress-linear v-model="buffer3" :buffer-value="bufferValue" color="light-blue darken-4" height="16"></v-progress-linear>
        <strong>Lighting & Rendering</strong>
        <v-progress-linear v-model="buffer3" :buffer-value="bufferValue" color="light-blue darken-4" height="16"></v-progress-linear>
      </v-flex>
      <v-flex xs12 sm12 md4 lg5 xl5 class="mx-2 pt-4">
        <h2>
          <span>Coding</span>
          <span class="light-blue--text text--darken-4">Skills</span>
        </h2>
        <br>
        <strong>VUE/VUEX</strong>
        <v-progress-linear  v-model="buffer4" :buffer-value="bufferValue" color="light-blue darken-4" height="16" ></v-progress-linear>
        <strong>HTML/CSS</strong>
        <v-progress-linear v-model="buffer5" :buffer-value="bufferValue" color="light-blue darken-4" height="16"></v-progress-linear>
        <strong>JavaScript</strong>
        <v-progress-linear v-model="buffer6" :buffer-value="bufferValue" color="light-blue darken-4" height="16"></v-progress-linear>
      </v-flex>
    </v-layout>
  </v-layout>
</template>

<script>
export default {

  data() {
    return {
      value: 0,
      buffer1: 0,
      buffer2: 0,
      buffer3: 0,
      buffer4: 0,
      buffer5: 0,
      buffer6: 0,
      bufferValue: 100,
      interval: 0
    };
  },
  mounted() {
    this.startBuffer();
  },

  beforeDestroy() {
    clearInterval(this.interval);
  },

  methods: {
    startBuffer() {
      this.interval = setInterval(() => {
        this.buffer1 = 98;
        this.buffer2 = 93;
        this.buffer3 = 90;
        this.buffer4 = 80;
        this.buffer5 = 90;
        this.buffer6 = 70;
      }, 600);
    }
  }
};
</script>
<style >
</style>

