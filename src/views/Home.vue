<template>
    <span>
        <home-opener></home-opener>
        <hello-world></hello-world>
    </span>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';
import HomeOpener from '@/components/HomeOpener.vue';

export default {
    name: 'Home',
    components: {
        HelloWorld,
        HomeOpener
    }
};
</script>
