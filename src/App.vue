<template>
  <div id="app">
    <h1>Music tastebreaker</h1>
    <hr>
    <Header
    v-bind:musicServices="musicServices"
    />
  </div>
</template>

<script>
import Header from '@/components/Header'

export default {
  name: 'App',
  data() {
    return {
      musicServices: [
        {id: 1, name: "Youtube music", url: "ex1.com"},
        {id: 2, name: "Spotify", url: "http://127.0.0.1:5000/api/spotify/url"},
        {id: 3, name: "Deezer", url: "ex3.com"},
      ]
    }
  },
  components: {
    Header
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
}
</style>
