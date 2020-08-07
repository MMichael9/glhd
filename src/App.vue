<template>
  <!-- <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/login">Login</router-link> |
      <router-link to="/services">Services</router-link>
    </div>
    <router-view />
  </div> -->

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
