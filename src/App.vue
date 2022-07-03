<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>
    Google one tap authorization example
  </h1>
  <GoogleOneTap />
</template>

<script>
import GoogleOneTap from './components/GoogleOneTap.vue'

export default {
  name: 'App',
  components: {
    GoogleOneTap
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
  margin-top: 60px;
}
</style>
