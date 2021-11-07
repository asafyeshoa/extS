<template>

<div>

  <v-img
        @mouseover="isHover = true"
        @mouseout="isHover = null"
      max-height="150"
      max-width="100"
      :src="pictureHover"
  ></v-img>

  <transition name="fade">
  <v-card
      @click="isHover = null"
      v-show="isHover"
      :loading="loading"
      class="mx-auto my-12"
      max-width="374"
  >
    <template slot="progress">
      <v-progress-linear
          color="deep-purple"
          height="10"
          indeterminate
      ></v-progress-linear>
    </template>

    <v-img
        height="250"
        :src=displayPhoto
    ></v-img>

    <v-card-text>
      <div>
        <v-list-item-icon class="iconHolder" >
          <v-icon>mdi-send</v-icon>
        </v-list-item-icon>

        <v-list-item-icon class="iconHolder" >
          <v-icon>+</v-icon>
        </v-list-item-icon>

        <v-list-item-icon class="iconHolder" >
          <v-btn
              class="ma-2"
              text
              icon
              color="red lighten-2"
          >
            <v-icon>mdi-thumb-down</v-icon>
          </v-btn>
        </v-list-item-icon>
        <v-list-item-icon class="iconHolder" >
          <v-btn
              class="ma-2"
              text
              icon
              color="blue lighten-2"
          >
            <v-icon>mdi-thumb-up</v-icon>
          </v-btn>
        </v-list-item-icon>
      </div>
      <div>
        <p>Match 98% 18+</p>
      </div>
      <div>
        <p>Well know soundtrack * Action * 2008</p>
      </div>
    </v-card-text>


  </v-card>
  </transition>
</div>

</template>

<script>
export default {
  name: 'HelloWorld',
  data: () => ({
    loading: false,
    selection: 1,
    displayPhoto: require("../assets/neeson_b.jpg"),
    photoStatic: require("../assets/3565.jpg"),
    videoCard:require("../assets/1.png"),
    isHover: null

  }),

  methods: {
    reserve () {
      this.loading = true

      setTimeout(() => (this.loading = false), 2000)
    },
  },
  computed: {
    pictureHover () {
      if (this.hover === true) {
        return this.videoCard
      } else {
        return this.photoStatic
      }
    }
  }
}
</script>

<style scoped >

.iconHolder {
  margin: 0;
  padding: 0;
}


.fade-enter-active {
  transition: all .3s ease;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}


</style>




