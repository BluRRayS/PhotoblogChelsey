<template>
  <div>
    <v-footer padless absolute dark color="grey darken-3" app>
      <v-card flat color="grey darken-3" class="flex">
        <v-card-title class="font-weight-light px-10">
        Follow me on social media!
        <v-spacer></v-spacer>
        <v-btn v-for="icon in icons" :key="icon" v-bind:href="icon.link" class="mx-4" dark icon>
          <v-icon size="24px">{{ icon.icon }}</v-icon>
        </v-btn>
        </v-card-title>

        <v-card-text  class="grey darken-4 font-weight-thin py-4 text-center white--text">
          © {{ new Date().getFullYear() }} —
          <strong>Chelsey Koopman</strong>
        </v-card-text >
      </v-card>
    </v-footer>
  </div>
</template>

<script>
export default {
  name: "Footer",
  data: () => ({
    icons: [
      {
        icon: "mdi-facebook",
        link: "https://www.facebook.com/pages/category/Photographer/Photography-by-Chelsey-110252157395793/"
      },
      {
        icon: "mdi-instagram",
        link: "https://www.instagram.com/photography.camlc/"
      },
      
    ],
  }),
};
</script>

<style>
</style>