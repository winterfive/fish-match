<template>
  <v-container fluid pa-10>
  <!-- Header -->
    <v-app-bar
      app
      color="indigo darken-3"
      dark
      dense
    >
      <v-toolbar-title>Game Name</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-app-bar-nav-icon @click="openOptions"></v-app-bar-nav-icon>
    </v-app-bar>
    <!-- Cards -->
    <v-content>
      <v-layout row wrap>
        <v-flex v-for="c in 10" :key="c" class="border">           
          <Card/>
        </v-flex>
      </v-layout>
    </v-content>
    

    <v-navigation-drawer
      v-model="right"
      fixed
      right
      temporary
    ></v-navigation-drawer>

    <v-footer
      app
      color="indigo darken-3"
      class="white--text"
    >
      <span>Made with PIE</span>
      <v-spacer></v-spacer>
      <span>&copy; 2019</span>
    </v-footer>
    </v-container>
</template>

<script>
import Card from "./Card.vue";
  export default {
    components: {
      Card
    },
    props: {
      source: String,
    },
    data: () => ({
      drawer: null,
      right: false
    }),
    methods: {
      openOptions() {
        console.log("options clicked");
      }
    }
  }
</script>

<style lang="scss" scoped>
.border {
  border: solid 1px red;
}
</style>


