<template>
  <div class="home">
    <!-- Banner -->
    <v-parallax dark src="@/assets/childs.jpeg">
      <v-container align="center" justify="center">
        <v-row align="center" justify="center">
          <v-col class="text-center" cols="12">
            <div>
              <h1 class="display-1 font-weight-thin mb-4">Chelsey Koopman</h1>
              <h4 class="subheading">Photography</h4>
            </div>
          </v-col>
          <v-btn dark icon class="mx-auto" @click="$vuetify.goTo('#blogposts')">
            <v-icon size="24px" color="white">mdi-chevron-down</v-icon>
          </v-btn>
        </v-row>
      </v-container>
    </v-parallax>

    <!-- Blog posts -->
    <v-container class="pa-10" id="blogposts">
      <h3 class="text-center font-weight-light">Latest blog posts</h3>
      <v-divider />
      <v-row justify="center" align="center">
        <v-col cols="4" v-for="post in posts" :key="post.title">
          <v-card shaped raised elevation="5">
            <v-list-item>
              <v-list-item-avatar color="teal">
                <img src="@/assets/chelsey.jpeg" alt="Chelsey" />
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title class="headline">{{post.title}}</v-list-item-title>
                <v-list-item-subtitle>door Chelsey Koopman</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
            <v-img class="white--text align-end" height="250px" src="@/assets/joep.jpeg"></v-img>
            <v-card-subtitle class="pb-0">{{post.subtitle}}</v-card-subtitle>
            <v-card-text class="text--primary">
              <div>{{post.desc}}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn color="teal" text>Lees verder</v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      posts: [
        {
          title: "Zwart wit",
          subtitle: "Hoe maak in een goed portet",
          desc:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores, vero!",
          img: "joep.jpeg",
        },
        {
          title: "Zwart wit",
          subtitle: "Hoe maak in een goed portet",
          desc:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores, vero!",
          img: "joep.jpeg",
        },
        {
          title: "Zwart wit",
          subtitle: "Hoe maak in een goed portet",
          desc:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores, vero!",
          img: "joep.jpeg",
        },
        {
          title: "Zwart wit",
          subtitle: "Hoe maak in een goed portet",
          desc:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores, vero!",
          img: "joep.jpeg",
        },
      ],
    };
  },
};
</script>
