<template>
  <div>
  <v-img
      v-show="ifHover === null"
      @mouseover="ifHover = true"
      @mouseout="ifHover = null"
      max-height="150"
      max-width="100"
      :src="photoStatic"
  ></v-img>

  <v-img
      v-show="ifHover === true"
      max-height="150"
      max-width="100"
      :src="pictureGif"
  ></v-img>

  </div>
</template>

<script>
export default {
  name: "videoTambnail",
  data() {
    return {
      photoStatic: require("../assets/3565.jpg"),
      pictureGif:require("../assets/1.png"),
      ifHover: null
    }
  }
}
</script>

<style scoped>

</style>
