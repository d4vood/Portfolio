<template>
  <div>
    <v-navigation-drawer v-model="drawer" absolute temporary app width="150" height="340">
      <v-list class="pt-4">
        <v-list-tile active-class="light-blue--text text--darken-4" to="/">
          <v-list-tile-content>
            <v-list-tile-title>HOME</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-list-tile active-class="light-blue--text text--darken-4" to="/resume">
          <v-list-tile-content>
            <v-list-tile-title>RESUME</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-list-tile active-class="light-blue--text text--darken-4" to="/services">
          <v-list-tile-content>
            <v-list-tile-title>SKILLS</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-list-tile active-class="light-blue--text text--darken-4" to="/portfolio">
          <v-list-tile-content>
            <v-list-tile-title>PORTFOLIO</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-list-tile active-class="light-blue--text text--darken-4" to="/contact">
          <v-list-tile-content>
            <v-list-tile-title>CONTACT</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar flat dense color="transparent" scroll-off-screen>
      <v-toolbar-side-icon class="hidden-md-and-up" @click.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title class="headline">
        <span class="font-weight-bold">Abror</span>
        <span class="light-blue--text text--darken-4">Akhmadiy</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn flat to="/" active-class="blue--text text--darken-4 headline">Home</v-btn>
        <v-btn flat to="/resume" active-class="blue--text text--darken-4 headline">Resume</v-btn>
        <v-btn flat to="/services" active-class="blue--text text--darken-4 headline">Skills</v-btn>
        <v-btn flat to="/portfolio" active-class="blue--text text--darken-4 headline">Portfolio</v-btn>
        <v-btn flat to="/contact" active-class="blue--text text--darken-4 headline">Contact</v-btn>
      </v-toolbar-items>
    </v-toolbar>
  </div>
</template>

<script>
export default {
  props: {
    goDark: {
      type: Boolean
    }
  },
  data() {
    return {
      drawer: null
    };
  },
};
</script>

<style >
</style>
