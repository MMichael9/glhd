<template>

  <v-app>
    <app-navigation class="app-nav"></app-navigation>

    <v-content transition="slide-x-transition">
      <router-view></router-view>
    </v-content>
  </v-app>


</template>

<script>
import AppNavigation from '@/components/AppNavigation';

export default {
  name: 'App',
  components: {
    AppNavigation
  }
};

</script>

<style>

</style>
