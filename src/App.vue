<template>
  <v-app>
    <SystemBar />

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import SystemBar from './components/SystemBar.vue'

export default {
  name: 'App',
  components: {
    SystemBar
  },
  data: () => ({
    //
  }),
};
</script>

<style>
  body::-webkit-scrollbar {
    display: none; /* for Chrome, Safari, and Opera */
  }
</style>
