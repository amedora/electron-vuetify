<template>
  <div id="app">
    <v-app>
      <v-navigation-drawer v-model="drawer"
        app
        fixed
        :clipped-left="$vuetify.breakpoint.mdAndUp"
        />
      <v-toolbar app dense fixed :clipped-left="$vuetify.breakpoint.mdAndUp">
        <v-toolbar-title style="width: 300px" class="ml-0 pl-3">
          <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
          <span class="hidden-sm-and-down">App Name</span>
        </v-toolbar-title>
      </v-toolbar>

      <v-content>
        <v-container fluid>
          <router-view />
        </v-container>
      </v-content>
      <v-footer app />
    </v-app>
  </div>
</template>

<script>
  export default {
    name: 'electron-vuetify',
    data () {
      return {
        drawer: null
      }
    }
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css?family=Roboto:300,400,500,700|Material+Icons');
  /* CSS */
</style>
