<template>
    <v-container>
        <v-toolbar color="white">
            <v-btn class="white" to="/profile">Home</v-btn>
            <v-spacer></v-spacer>
            <v-btn class="white" to="/profile/account">My Profile</v-btn>
            <v-spacer></v-spacer>
            <v-btn class="error" to="/">Logout</v-btn>
        </v-toolbar>
    </v-container>
</template>
<script>
export default {
    name: 'ProfileNavigation'
};
</script>
<style scoped>

</style>
