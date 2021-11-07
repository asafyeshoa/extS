<template>
  <v-app>
    <v-app-bar
      app
      color="red darken-2"
      dark
    >

      <v-spacer></v-spacer>


    </v-app-bar>

    <v-main>
      <div class="container">
      <videoCard/>
      </div>
    </v-main>
  </v-app>
</template>

<script>
import videoCard from './components/videoCard';


export default {
  name: 'App',

  components: {
    videoCard,
  },

  data: () => ({
    //
  }),
};
</script>

<style scoped>

</style>
