<template>
    <v-container class="fill-height" fluid>
        <v-row align="center" justify="center">
            <v-col cols="12" xs="12" sm="10" md="6" lg="4">
                <v-card class="elevation-12">
                    <v-toolbar color="primary" dark flat>
                        <v-spacer></v-spacer>
                        <v-toolbar-title>Login</v-toolbar-title>
                        <v-spacer></v-spacer>
                    </v-toolbar>
                    <v-card-text>
                        <v-form @submit.prevent="loginUser" id="check-login-form">
                            <v-text-field
                                label="Login"
                                name="login"
                                prepend-icon="mdi-account"
                                type="text"
                                v-model="login.email"
                            ></v-text-field>

                            <v-text-field
                                id="password"
                                label="Password"
                                name="password"
                                prepend-icon="mdi-lock"
                                type="password"
                                v-model="login.password"
                            ></v-text-field>
                            <v-card-actions>
                                <v-spacer></v-spacer>
                                <v-btn color="primary" type="submit" form="check-login-form">Login</v-btn>
                            </v-card-actions>
                        </v-form>
                    </v-card-text>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    data() {
    return {
      login: {
        email: "",
        password: ""
      }
    };
  },
  methods: {
      async loginUser() {
      try {
          console.log("TEST");
        let response = await this.$http.post("/user/login", this.login);
        let token = response.data.token;
        localStorage.setItem("jwt", token);
        if (token) {
          console.log("Success", "Login Successful", "success");
          this.$router.push("/profile");
        }
      } catch (err) {
        console.log("Error", "Something Went Wrong", "error");
        console.log(err.response);
      }
    }
  }
};
</script>

<style scoped></style>
