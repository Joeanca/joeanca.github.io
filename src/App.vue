<template>
  <div id="app">
    <v-toolbar class="white">
      <v-toolbar-title v-text="title"></v-toolbar-title>
    </v-toolbar>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
  data () {
        return {
            title: 'Your Logo'
        }
    }
}
</script>

<style>
</style>
