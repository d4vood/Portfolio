<template>
  <v-container grid-list-xl>
    <v-layout row align-center wrap class="mt-4 pt-2">
      <v-flex xs12 sm12 md6 lg6 xl6>
        <h2 class="pb-4 mt-2">
          <span>Contact</span>
          <span class="light-blue--text text--darken-4">Info</span>
        </h2>
        <div class="py-4 subheading font-weight-bold">
          <v-icon large color="light-blue darken-4" left>fas fa-map-marker-alt</v-icon>
          <span>Tashkent,&nbsp;</span>
          <span class="light-blue--text text--darken-4">Uzbekistan</span>
        </div>
        <div class="py-4 subheading font-weight-bold">
          <v-icon large color="light-blue darken-4" left>fas fa-envelope</v-icon>
          <span>abu.web.dev@</span>
          <span class="light-blue--text text--darken-4">gmail.com</span>
        </div>
        <div class="py-4 subheading font-weight-bold">
          <v-icon large color="light-blue darken-4" left>fas fa-phone</v-icon>
          <span>+20 </span>
          <span class="light-blue--text text--darken-4">155 359 4557</span>
        </div>
        <div class="py-4 subheading font-weight-bold">
          <v-icon large color="light-blue darken-4" left>fas fa-check</v-icon>
          <span>Freelance</span>
          <span class="light-blue--text text--darken-4">Available</span>
        </div>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import { validationMixin } from "vuelidate";
import {
  required,
  maxLength,
  email,
  minLength
} from "vuelidate/lib/validators";
export default {
  mixins: [validationMixin],
  validations: {
    name: { required, maxLength: maxLength(20) },
    email: { required, email },
    body: { required, minLength: minLength(20) }
  },
  data() {
    return {
      name: "",
      email: "",
      body: ""
    };
  },
  methods: {
    submit() {
      this.$v.$touch();
    },
    clear() {
      this.$v.$reset();
      this.name = "";
      this.email = "";
      this.body = "";
    }
  },
  computed: {
    nameErrors() {
      const errors = [];
      if (!this.$v.name.$dirty) return errors;
      !this.$v.name.maxLength &&
        errors.push("Name must be at most 20 characters long");
      !this.$v.name.required && errors.push("Name is required.");
      return errors;
    },
    emailErrors() {
      const errors = [];
      if (!this.$v.email.$dirty) return errors;
      !this.$v.email.email && errors.push("Must be valid e-mail");
      !this.$v.email.required && errors.push("E-mail is required");
      return errors;
    },
    bodyErrors() {
      const errors = [];
      if (!this.$v.body.$dirty) return errors;
      !this.$v.body.minLength &&
        errors.push("Text must be at least 20 characters long");
      !this.$v.body.required && errors.push("Text is required");
      return errors;
    }
  }
};
</script>

<style lang="scss" scoped>
</style>
