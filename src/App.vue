<template>
  <div id="app" style="background-image: url('./assets/bg5.jpg')">
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

<style src="./assets/css/styles.css" scoped></style>