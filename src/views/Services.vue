<template>
  <v-container grid-list-xl>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-flex xs12 sm12 md12 lg12 xl12>
        <h2 class="pl-4">
          <span>Web</span>
          <span class="light-blue--text text--darken-4">Skills</span>
        </h2>
      </v-flex>
      <v-flex v-for="service in services" :key="service.src" xs6 sm3 md3 lg3 xl3>
        <v-card hover flat color="transparent" :style="{'cursor':'context-menu'}">
          <v-card-title></v-card-title>
          <v-img
            :src="service.src"
            height="100"
            aspect-ratio="2.75"
            :alt="'Eldin do '+service.title"
            contain
          ></v-img>
          <v-card-title class="justify-center">
            <v-flex text-xs-center subheading font-weight-bold>{{service.title}}</v-flex>
          </v-card-title>
        </v-card>
      </v-flex>
      <v-flex xs12 sm12 md12 lg12 xl12>
        <h2 class="pl-4">
          <span>Design</span>
          <span class="light-blue--text text--darken-4">Skills</span>
        </h2>
      </v-flex>
      <v-flex v-for="design in designs" :key="design.src" xs6 sm3 md3 lg3 xl3>
        <v-card hover flat color="transparent" :style="{'cursor':'context-menu'}">
          <v-card-title></v-card-title>
          <v-img
              :src="design.src"
              height="100"
              aspect-ratio="2.75"
              :alt="'Eldin do '+design.title"
              contain
          ></v-img>
          <v-card-title class="justify-center">
            <v-flex text-xs-center subheading font-weight-bold>{{design.title}}</v-flex>
          </v-card-title>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      services: [
        {
          src: require("../assets/html5.png"),
          title: "DOM, Events"
        },
        {
          src: require("../assets/css3.png"),
          title: "Responsive layout,\n" +
              "Animations"
        },
        {
          src: require("../assets/JS.png"),
          title: "ES6 syntax"
        },
        {
          src: require("../assets/bootstrap.png"),
          title: "Grid system"
        },
        {
          src: require("../assets/vue.png"),
          title: "Vue Router, Vuex,\n" +
              "Vuetify"
        }
      ],
      designs: [
        {
          src: require("../assets/maya.png"),
          title: "Maya"
        },
        {
          src: require("../assets/max.png"),
          title: "3ds Max"
        },
        {
          src: require("../assets/zbrush.png"),
          title: "ZBrush"
        },
        {
          src: require("../assets/speedtree.png"),
          title: "SpeedTree"
        },
        {
          src: require("../assets/sbtance.png"),
          title: "Substance Painter"
        },
        {
          src: require("../assets/ps.png"),
          title: "Photoshop"
        },
        {
          src: require("../assets/ae.png"),
          title: "After Effects"
        },
      ]
    };
  }
};
</script>
<style >
.v-img--reveal {
  opacity: 0.3;
}
</style>
