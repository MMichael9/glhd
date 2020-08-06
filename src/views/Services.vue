<template>
     <div class="Services">
       <test msg= "We offer the following services:" />
     </div>
</template>

<script>
// @ is an alias to /src
import test from "@/components/test.vue";

export default {
  name: "Services",
  components: {
    test
  }
};
</script>