<template>
  <div class="home">
    <h1>Homepage</h1>
    <!-- Breakpoints means the display/device size, Visibility means if we only want to show it in large device/ small etc that kind of stuff-->
    
    <!-- <v-btn class="hidden-md-and-down">click me</v-btn> -->
    <!-- <v-btn class="hidden-md-and-up">click me</v-btn> -->
    <v-btn class="hidden-sm-only">click me</v-btn>

  </div>
</template>

<script>
export default {
  name: 'Home',
}
</script>
