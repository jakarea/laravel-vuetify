<template>
  <div id="app">
    <v-app id="inspire" dark>
      <v-navigation-drawer
        clipped
        fixed
        class="orange accent-2"
        v-model="drawer"
        app
      >
        <v-list dense>
          <v-list-tile @click="">
            <v-list-tile-action>
              <v-icon>dashboard</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title>Dashboard</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
          <v-list-tile @click="">
            <v-list-tile-action>
              <v-icon>settings</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title>Settings</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </v-list>
      </v-navigation-drawer>
      
      <v-toolbar app fixed clipped-left class="orange accent-2">
        <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
        <v-toolbar-title>M/S. Abul Monsur Khan</v-toolbar-title>
      </v-toolbar>
      <v-content>
        <v-container fluid>
          <v-layout justify-center align-center>
            <router-view></router-view>
          </v-layout>
        </v-container>
      </v-content>
      <v-footer app fixed>
        <span>&copy; 2017</span>
      </v-footer>
    </v-app>
  </div>
</template>

<script>
// import bredcumb from './components/common/Bredcumb'
export default {
  name: 'app',
  data: () => ({
    drawer: true
  })
}
</script>
