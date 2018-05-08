<template>
  <v-flex shrink>
      <!-- search -->
      <v-card dark class="pt-3">
          <v-layout row wrap>
              <v-flex xs12 sm4 class="px-2">
                  <v-btn @click="" class="orange accent-2" dark>
                      New User
                      <v-icon right dark>add</v-icon>
                  </v-btn>
              </v-flex>
              <v-flex xs12 sm8 class="px-2 text-xs-center text-sm-right">
                  <v-btn @click="" class="orange accent-2" dark>
                      Manage Groups <v-icon right dark>group</v-icon>
                  </v-btn>
                  <v-btn @click="" class="orange accent-2" dark>
                      Manage Permissions <v-icon right dark>vpn_key</v-icon>
                  </v-btn>
              </v-flex>
              <v-flex class="my-2"><v-divider></v-divider></v-flex>
              <v-spacer></v-spacer>
              <v-flex class="px-2">
                  <v-text-field prepend-icon="search" dark color="orange accent-2" label="Filter By Name"></v-text-field>
              </v-flex>
              <v-flex class="px-2">
                  <v-text-field prepend-icon="search" dark color="orange accent-2" label="Filter By Email"></v-text-field>
              </v-flex>
          </v-layout>
      </v-card>
      <!-- /search -->
  </v-flex>
</template>

<script>
  export default {
    data: () => ({
      drawer: true
    }),
    props: {
      source: String
    }
  }
</script>
