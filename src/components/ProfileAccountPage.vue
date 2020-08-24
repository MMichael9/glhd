<template>
    <span>
        <profile-navigation></profile-navigation>
        <v-container>
            <v-card elevation=12>
                <p>Account Page</p>
            </v-card>
        </v-container>
    </span>
</template>

<script>
import ProfileNavigation from '@/components/ProfileNavigation';

export default {
    name: 'ProfileAccountPage',
    components: {
        ProfileNavigation
    }
};
</script>

<style></style>
