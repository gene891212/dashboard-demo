<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      app
    >
      <Navigation />
    </v-navigation-drawer>

    <v-app-bar app>
      <v-app-bar-nav-icon @click="changeDrawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Application</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <HelloWorld />
      <HelloWorld />
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Navigation from "./components/Navigation.vue";

export default {
  name: "App",

  components: {
    HelloWorld,
    Navigation,
  },

  data() {
    return {
      drawer: false,
    };
  },
  methods: {
    changeDrawer: function () {
      this.drawer = !this.drawer;
      console.log(this.drawer);
    },
  },
};
</script>
