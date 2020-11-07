<template>
  <div class="home">
    <h1>Homepage</h1>
    <v-btn class="pink white--text ml-3">Click me</v-btn>
    <v-btn depressed color="pink ml-3">Click me</v-btn>
    <v-btn text color="pink ml-3">Click me</v-btn>  
    <v-btn primary class="ml-3">Click me</v-btn>
    
    <br><br>

    <v-btn large class="pink white--text ml-3">
      <v-icon large left>mdi-email</v-icon>
      <span>email</span>
    </v-btn>
    
    <v-btn small class="pink white--text ml-3">
      <v-icon small left>mdi-email</v-icon>
      <span>email</span>
    </v-btn>

    <v-btn class="pink white--text mx-3">
      <span>email</span>
      <v-icon right>mdi-email</v-icon>
    </v-btn>

    <v-btn fab dark color="purple">
      <v-icon>mdi-heart</v-icon>
    </v-btn>
  </div>
</template>

<script>
export default {
  name: 'Home',
}
</script>
