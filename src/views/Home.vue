<template>
  <v-layout column justify-center align-center class="mt-4 pt-2">
    <VueCompareImage
      class="hidden-md-and-down"
      hover
      :style="{ minWidth: '1300px' }"
      :sliderLineWidth="sliderLine"
      :handleSize="hSize"
      :leftImage="image1"
      :rightImage="image2"
      :sliderPositionPercentage="sliderPosition"
    />
    <VueCompareImage
      class="hidden-lg-and-up"
      hover
      :style="{ maxWidth: '400px' }"
      :sliderLineWidth="sliderLine"
      :handleSize="hSize"
      :leftImage="image1"
      :rightImage="image2"
      :sliderPositionPercentage="sliderPosition"
    />

    <br>

    <vue-typer class="headline" :repeat="0" text="Davud Yusupov"></vue-typer>
    <vue-typer
      :text="text1"
      :repeat="Infinity"
      :shuffle="false"
      initial-action="erasing"
      :pre-type-delay="70"
      :type-delay="70"
      :pre-erase-delay="1980"
      :erase-delay="150"
      erase-style="select-back"
      :erase-on-complete="false"
      caret-animation="smooth"
    ></vue-typer>
    <br>
    <v-flex xs12 sm6 md4 lg4 xl4>
      <v-card flat color="transparent" max-width="500">
        <v-card-title primary-title>
          <div>
            <h3 class="headline mb-0">
              <span>About</span>
              <span class="light-blue--text text--darken-4">Me</span>
            </h3>
            <div>
              <p>
                Hello! I’m <span
                  class="light-blue--text text--darken-4"
              >Davud Yusupov</span>. I’m a professional 3d designer with over 6 years of
                work experience, moving to web development.
                Since I started my career in IT, I have been
                progressing and working on myself and I have
                always been interested in software engineering.
                One year ago, I totally switched myself to web
                development. Since I attended a 100+ hour coding
                courses. Fast learner, ready to apply my passion
                for coding to a talented engineering team to
                develop quality solutions.
              </p>
            </div>
          </div>
        </v-card-title>

      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import { VueTyper } from "vue-typer";
import VueCompareImage from "vue-compare-image";
import image1 from "../assets/image1.jpg"
import image2 from "../assets/image2.jpg"

export default {
  components: {
    "vue-typer": VueTyper,
    VueCompareImage
  },
  data() {
    return {
      text1: ["Front-End Developer", "3D Designer"],
      leftImage: require("../assets/image1.jpg").default,
      rightImage: require("../assets/image2.jpg").default,
      leftImage2: require("../assets/image1.jpg").default,
      rightImage2: require("../assets/image2.jpg").default,
      sliderLine: 0,
      hSize: 0,
      sliderPosition: 0.5,
      image1,
      image2,
    };
  }
};
</script>
<style>
@keyframes rocking {
  0%,
  100% {
    transform: rotateZ(-10deg);
  }

  50% {
    transform: rotateZ(10deg);
  }
}

.vue-typer {
  font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
}
.vue-typer .custom.char.typed {
  color: #01579b;
}
.vue-typer .custom.char.selected {
  color: #e30505;
}

.vue-typer .custom.caret {
  animation: rocking 1s ease-in-out 0s infinite;
}
.vue-typer .custom.caret.typing {
  background-color: #01579b;
}
.vue-typer .custom.caret.selecting {
  display: inline-block;
  background-color: #e91e63;
}
</style>

