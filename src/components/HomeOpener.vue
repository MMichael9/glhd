<template>
    <v-container fluid fill-height class="home-hero" style="max-height: 100vh">
        <v-layout justify-center align-center column pa-5>
            <div class="display-4 font-weight-black white--text text-xs-center">
                Good Look
            </div>
            <div
                class="display-4 font-weight-black white--text text-xs-center mb-3"
            >
                Hair Design
            </div>
            <div
                class="display-1 font-weight-bold white--text text-xs-center"
            ></div>
            <div class="display-1 font-weight-bold white--text text-xs-center">
                Professional hair salon in Queensborough since 1998.
            </div>
            <div>
                <v-btn rounded="true" id="book-now" to="/login"
                    >Book Appointment</v-btn
                >
            </div>
        </v-layout>
    </v-container>
</template>

<script>
export default {
    name: 'HomeOpener'
};
</script>

<style scoped>
.home-hero {
    background: url('../assets/home_opener.jpg');
    background-size: cover;
    width: 100%;
    height: 100%;
}

#book-now {
    background-color: red;
    color: white;
    margin-top: 70%;
}
</style>
