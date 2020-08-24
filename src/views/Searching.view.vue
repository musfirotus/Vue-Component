<template>
  <div>
    <search />
    <selected-item />
  </div>
</template>

<script>
import Search from '../components/Search.vue'
import SelectedItem from '../components/SelectedItem.vue'

export default {
  name: 'Searching',
  components: {
    Search,
    SelectedItem
  }
}
</script>

<style>
</style>
