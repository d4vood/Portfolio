<template>
  <v-container grid-list-xl>
    <h2 class="pl-4">
      <span>Web</span>
      <span class="light-blue--text text--darken-4">Portfolio</span>
    </h2>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-dialog
        v-model="project.dialog"
        lazy
        max-width="1000"
        v-for="project in projects"
        :key="project.title"
      >
        <template v-slot:activator="{ on }">
          <v-flex xs12 sm6 md4 lg4 xl4 v-on="on">
            <v-card hover flat color="transparent">
              <v-img
                :src="project.poster"
                :alt="project.title"
                height="230"
                lazy-src="https://cdn.dribbble.com/users/1299339/screenshots/11116681/media/79bf1ac602445860e4a44bcd4bf80704.gif"
              ></v-img>
              <v-card-title primary-title class="justify-center">{{project.title}}</v-card-title>
            </v-card>
          </v-flex>
        </template>
        <v-card v-if="project.dialog">
          <v-img :src="project.poster"></v-img>
          <v-card-text>
            <h3 class="headline mb-0">
              <span>Technology</span>
            </h3>
            <v-chip color="light-blue darken-4" text-color="white">{{project.tech.tech1}}</v-chip>
            <v-chip color="light-blue darken-4" text-color="white">{{project.tech.tech2}}</v-chip>
            <v-chip color="light-blue darken-4" text-color="white">{{project.tech.tech3}}</v-chip>
          </v-card-text>
          <v-card-actions>
            <v-btn flat large dark color="light-blue darken-4" :href="project.git" target="_blank">
              <i class="fa-solid fa-laptop-code" style="font-size: 35px">Demo</i>
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      dialog: false,
      projects: [
         {
          dialog: false,
          title: "Todo-List",
          git: "https://todo-list-psi-black.vercel.app/",
          tech: {
            tech1: "Vue.js",
            tech2: "VUEX",
            tech3: "Materialize",
          },
          poster: require("@/assets/todo.png"),
        },
        {
          dialog: false,
          title: "Website-Clinic",
          git: "https://clinic-website-xi.vercel.app/",
          tech: {
            tech1: "Vue.js",
            tech2: "VUEX",
            tech3: "Vuetify",
            tech4: "Vue Router",
          },
          poster: require("@/assets/todo.png"),
        },
        {
          dialog: false,
          title: "Construction",
          git: "https://construction-five-ashen.vercel.app/",
          tech: {
            tech1: "HTML",
            tech2: "CSS",
            tech3: "Bootstrap",
          },
          poster: require("@/assets/construction.png"),
        },

      ]
    };
  }
};
</script>

<style  scoped>
</style>
