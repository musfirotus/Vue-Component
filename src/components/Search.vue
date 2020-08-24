<template>
  <div class="h-100 w-full flex items-center justify-center bg-teal-lightest font-sans -mb-12">
    <form class="w-full border border-purple-500 max-w-xs bg-white shadow-md rounded px-5 pt-5 pb-5 mb-4">
      <input v-model="searchValue" v-on:keyup="checkSearch" class="bg-white focus:outline-none focus:shadow-outline border border-gray-300 rounded-lg py-2 px-4 block w-full appearance-none leading-normal" type="text" placeholder="Insert Title">
      <h1 class="mt-3 mb-3">{{message}} </h1>
      <p class="max-w-xl text-center text-gray-600 text-xs">
        Coded by Musfirotus
      </p>
    </form>
    <!-- <h4 class="mt-3 mb-3" v-if="cari.length >= 1 && cari.length <= 2">Loading...</h4>
      <h4 class="mt-3 mb-3">{{message}}</h4> -->
  </div>
</template>

<script>
export default {
  name: 'Search',
  props: ["message"],
  data: function() {
    return {
      searchValue: "",
    }
  },
  methods: {
    checkSearch: function(){
      this.$emit("new-search", this.searchValue)
    }
  }
}
</script>

<style src="../assets/css/styles.css"></style>