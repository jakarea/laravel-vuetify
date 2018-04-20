<template>
  <v-app id="inspire">
    <v-content>
      <v-container fluid fill-height>
        <v-layout align-center justify-center>
          <v-flex xs12 sm8 md4>
            <v-card class="elevation-12">
              <v-toolbar dark color="orange accent-4">
                <v-toolbar-title>M/S ABUL MONSUR KHAN</v-toolbar-title>
                <v-spacer></v-spacer>
                <v-tooltip bottom>
                  <v-btn
                    icon
                    large
                    href="/"
                    target="_blank"
                    slot="activator"
                  >
                  <v-icon large >home</v-icon>
                  </v-btn>
                </v-tooltip>
              </v-toolbar>
              <v-card-text>
                <p class="red--text text-md-center"></p>
                <v-form>
                  <v-text-field
                    prepend-icon="person"
                    label="E-mail"
                    v-model="email"
                    :rules="emailRules"
                    hint="Enter your email"
                    color="orange accent-4"
                    required
                  >
                  </v-text-field>

                  <v-text-field
                    prepend-icon="lock"
                    label="Password"
                    v-model="password"
                    :rules="passwordRules"
                    hint="At least 6 characters"
                    min="6"
                    type="password"
                    color="orange accent-4"
                    required
                  >
                  </v-text-field>

                  <v-text-field
                    prepend-icon="lock"
                    label="Confirm Password"
                    v-model="confirmpassword"
                    :rules="confirmpasswordRules"
                    hint="Confirm password should match with password"
                    min="6"
                    type="password"
                    color="orange accent-4"
                    required
                  >
                  </v-text-field>

                </v-form>
              </v-card-text>
              <v-card-actions>
                <router-link to="login">Allready have account?</router-link>
                 <v-spacer></v-spacer>
                <v-btn dark color="orange accent-4" @click="submit">Register</v-btn>
              </v-card-actions>
            </v-card>
          </v-flex>
        </v-layout>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
  export default {
    data: () => ({
      email: null,
      password: null,
      rememberme: null,
      confirmpassword: null,
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/.test(v) || 'E-mail must be valid'
      ],
      emailError: null,
      passwordRules: [
        v => !!v || 'Password is required'
      ],
      passwordError: null,
      confirmpasswordRules: [
        v => !!v || 'Password is required'
      ],
      confirmpasswordError: null
    }),
    methods: {
      submit () {
      }
    }
  }
</script>
