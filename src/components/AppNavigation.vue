<template>
    <span>
        <v-navigation-drawer
            app
            v-model="drawer"
            class="blue lighten-2"
            dark
            disable-resize-watcher
            right
        >
            <v-list>
                <template v-for="(item, index) in items">
                    <v-list-item :key="index" :to="item.url">
                        <v-list-item-content>{{
                            item.title
                        }}</v-list-item-content>
                    </v-list-item>
                    <v-divider :key="`divider-${index}`"></v-divider>
                </template>
            </v-list>
        </v-navigation-drawer>
        <v-toolbar app color="blue darken-4" dark>
            <router-link to="/">
                <v-toolbar-title class="title">{{ appTitle }}</v-toolbar-title>
            </router-link>
            <v-btn class="hidden-sm-and-down btn" to="/services"
                >Services</v-btn
            >
            <v-btn class="hidden-sm-and-down btn" to="/about">About Us</v-btn>
            <v-btn class="hidden-sm-and-down btn">Contact Us</v-btn>
            <!-- Contact us in home ? -->
            <v-spacer class="hidden-sm-and-down"></v-spacer>
            <v-btn flat class="hidden-sm-and-down" to="/login">SIGN IN</v-btn>
            <v-btn color="blue lighten-2" class="hidden-sm-and-down" to="/join"
                >JOIN</v-btn
            >
            <v-spacer class="hidden-md-and-up"></v-spacer>
            <v-toolbar-side-icon
                class="hidden-md-and-up test"
                @click="drawer = !drawer"
            >
                <v-icon>list menu</v-icon>
            </v-toolbar-side-icon>
        </v-toolbar>
    </span>
</template>
<script>
export default {
    name: 'AppNavigation',
    data() {
        return {
            appTitle: 'GLHD',
            drawer: false,
            items: [
                { title: 'Services', url: '/services' },
                { title: 'Sign In', url: '/login' },
                { title: 'Join', url: '/join' },
                { title: 'About Us', url: '/about' },
                { title: 'Contact Us', url: '/contact' }
            ]
        };
    }
};
</script>
<style scoped>
a {
    color: white;
    text-decoration: none;
}
.btn {
    margin: 10px;
}

.title {
    color: white;
    text-decoration: white;
}
</style>
