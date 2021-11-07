<template>
  <v-img
      max-height="300"
      max-width="250"
      :src="pictureHover"

      @mouseover="hover = true"
      @mouseleave="hover = false"
  ></v-img>
</template>

<script>
export default {
  name: "videoIMg",
  data() {
    return {
      pictureGif:require("../assets/1.png"),
      photoStatic: require("../assets/2.jpg"),
      hover: false
    }
  },
  computed: {
    pictureHover () {
      if (this.hover === true) {
        return this.pictureGif
      } else {
        return this.photoStatic
      }
    }
  }
}
</script>

<style scoped>

</style>
<!--      @mouseover="isHover = true"-->
<!--      @mouseout="isHover = null"-->
