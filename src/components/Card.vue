<template>
  <v-content class="card"/>
</template>

<script>
export default {
  name: "Card"
};
</script>

<style scoped lang="scss">
.card {
    background-color: blue;
    border-radius: 10px;
    height: 240px;
    width: 140px;
    margin: 20px;
}

.card:hover {
  background-color: green;
}
</style>
