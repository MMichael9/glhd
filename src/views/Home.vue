<template>
  <div class="home">
    <img alt="gl logo" src="../assets/gl2.jpg" />
    <HelloWorld msg="GLHD" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    HelloWorld
  }
};
</script>
