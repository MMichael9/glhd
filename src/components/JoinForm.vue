<template>
    <v-container fluid>
        <v-layout justify-center align-center> 
            <v-row align="center" justify="center">
            <v-col cols="12" xs="12" sm="10" md="6" lg="4">
                <v-card class="elevation-12">
                    <v-toolbar color="primary" dark flat>
                        <v-spacer></v-spacer>
                        <v-toolbar-title>Sign Up</v-toolbar-title>
                        <v-spacer></v-spacer>
                    </v-toolbar>
                    <v-card-text>
                        <v-form @submit.prevent="signUpUser" id="check-signup-form">
                            <v-text-field
                                label="First Name"
                                name="fname"
                                prepend-icon="mdi-account"
                                type="text"
                                v-model="signup.firstName"                                
                            ></v-text-field>
                            <v-text-field
                                label="Last Name"
                                name="lname"
                                prepend-icon="mdi-account"
                                type="text"
                                v-model="signup.lastName"
                            ></v-text-field>
                            <v-text-field
                                label="Email Address"
                                name="email"
                                prepend-icon="mdi-account"
                                type="text"
                                v-model="signup.email"
                            ></v-text-field>
                            <v-text-field
                                label="Phone Number"
                                name="phoneNumber"
                                prepend-icon="mdi-account"
                                type="text"
                                v-model="signup.phoneNumber"
                            ></v-text-field>
                            <v-text-field
                                id="password"
                                label="Password"
                                name="password"
                                prepend-icon="mdi-lock"
                                type="password"
                                v-model="signup.password"
                            ></v-text-field>
                            <v-text-field
                                id="confirmPassword"
                                label="Confirm Password"
                                name="confirmPassword"
                                prepend-icon="mdi-lock"
                                type="password"
                            ></v-text-field>
                            <v-card-actions>
                                <v-spacer></v-spacer>
                                <v-btn color="primary" type="submit" form="check-signup-form">Sign Up</v-btn>
                            </v-card-actions>
                        </v-form>
                    </v-card-text>
                </v-card>
            </v-col>
            </v-row>
        </v-layout>
    </v-container>
</template>

<script>
export default {
    name: 'JoinForm',
    data() {
        return {
            signup: {
                firstName: "",
                lastName: "",
                email: "",
                phoneNumber: "",
                password: ""
            }
        }
    },
    methods: {
        async signUpUser() {
            try {
                let response = await this.$http.post("/user/register", this.signup);
                console.log(response);
                let token = response.data.token;
                if (token) {
                    localStorage.setItem("jwt", token);
                    this.$router.push("/");
                    console.log("Success", "Registration Was successful", "success");
                } else {
                    console.log("Error", "Something Went Wrong", "error");
                }
            }
            catch (err) {
                let error = err.response;
                if (error.status == 409) {
                console.log("Error", error.data.message, "error");
                } else {
                console("Error", error.data.err.message, "error");
                }
            }
        }
    }
};
</script>

<style scoped>

</style>
