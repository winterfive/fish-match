<script>
import Card from "./Card";

export default {
  name: "Game",
  components: {
    Card
  }   
}
</script>

<template>
  <v-container>
    <v-select>
      <header>Game Name</header>
    </v-select>
    <v-select row wrap>
      <v-flex>
        <v-card v-for="c in 10" :key="c"><Card/></v-card>
      </v-flex>
    </v-select>
  </v-container>
</template>

<style lang="scss" scoped>

</style>


