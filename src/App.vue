<template>
  <div id="app">
    <h1>Music tastebreaker</h1>
    <hr>
    <Header
    v-bind:musicServices="oauthClients"
    />
  </div>
</template>

<script>
import Header from '@/components/Header'
import axios from 'axios'

export default {
  name: 'App',
  data() {
    return {
      oauthClients: null
    }
  },
  mounted() {
    axios
        .get('http://127.0.0.1:5000/api/oauth_clients')
        .then(response => (this.oauthClients = response.data.info));
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
