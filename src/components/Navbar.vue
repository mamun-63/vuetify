<template>
  <nav>
    <v-app-bar flat>
      <v-app-bar-nav-icon color="grey" @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>
        <span class="font-weight-light">Todo</span>
        <span>Vuetify</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text color="grey"> 
        <span>sign out</span>
        <v-icon right>mdi-exit-to-app</v-icon>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" app temporary class="primary">
      <p class="info">App</p>
    </v-navigation-drawer>

  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  data() {
    return {
      drawer: false
    }
  }
}
</script>

