<template>
  <v-container grid-list-xl>
    <h2 class="pl-4">
      <span>Graphic</span>
      <span class="light-blue--text text--darken-4">Portfolio</span>
    </h2>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-flex  v-for="design in designs" :key="design.src" xs6 sm3 md3 lg3 xl3>
        <v-card  hover flat color="transparent" :style="{'cursor':'context-menu'}">
          <v-card-title></v-card-title>
          <v-img
              :src="design.src"
              height="150"
              aspect-ratio="2.75"
              :alt="'Eldin do '+design.title"
              contain
          ></v-img>
          <v-card-title class="justify-center">
            <v-flex text-xs-center subheading font-weight-bold>{{design.title}}</v-flex>
            <v-btn large flat dark color="light-blue darken-4" :href="design.link" target="_blank">
              <i class="fa-brands fa-youtube" style="font-size: 35px"></i>
            </v-btn>
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
      designs: [
        {
          src: require("@/assets/3d.png"),
          title: "Commercial Projects",
          link: "https://youtu.be/1XGamOlZukc"
        },
        {
          src: require("@/assets/3d2.png"),
          title: "Test Projects",
          link: "https://youtu.be/TOpw31962XI"
        },
      ]
    };
  }
};
</script>

<style  scoped>
</style>
