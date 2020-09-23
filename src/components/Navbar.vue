<template>
  <div>
    <!-- Nav drawer -->
    <v-navigation-drawer dark disable-resize-watcher  app v-model="drawer" right class="dark">
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title">
            <span class="font-weight-thin">Chelsey Koopman </span>        
          </v-list-item-title>
           <v-list-item-title class="title">
            <span>Photography</span>        
          </v-list-item-title>
        </v-list-item-content>
      </v-list-item>
      <v-divider></v-divider>
      <v-list dense nav>
        <v-list-item v-for="item in links" :key="item.title" link router :to="item.route">
        
            <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <!-- Nav bar -->
    <v-app-bar dark app>
      <router-link to="/" tag="span" style="cursor: pointer" class="pr-6">
        <v-toolbar-title class="text-uppercase white--text">
          <span class="font-weight-thin">Chelsey Koopman </span>
          <span>Photography</span>
        </v-toolbar-title>
      </router-link>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn primary dark text v-for="item in links" :key="item.title" :to="item.route">
          {{ item.title }}
        </v-btn>
      </v-toolbar-items>
      <v-spacer></v-spacer>
      
      <v-app-bar-nav-icon class="hidden-md-and-up" @click="drawer = !drawer"></v-app-bar-nav-icon>
    </v-app-bar>


  </div>
</template>

<script>
export default {
  name: "Navbar",
   data () {
      return {
        drawer: false,
        links: [
        {
          title: "Home",
          route: "/",
        },
        {
          title: "Blog",
          route: "/blog"
        },
        {
          title: "About",
          route: "/about",
        },
        {
          title: "Contact",
          route: "/contact",
        },
      ],
      }
   }
};
</script>

<style>
</style>