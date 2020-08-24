<template>
  <div id="app">
    <searching />
  </div>
</template>

<script>
import Searching from './views/Searching.view'

export default {
  name: 'App',
  components: {
    Searching
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
