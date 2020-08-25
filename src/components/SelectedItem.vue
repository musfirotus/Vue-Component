<template>
  <div class="h-100 w-full flex items-center justify-center font-sans">
    <div class="border border-white-500 w-full bg-blue-500 shadow-md rounded pt-6 pb-8 px-5">
      <h3 class="text-center font-bold mb-5 text-4xl text-black bg-blue-300">Selected Item</h3>
      <div v-if="this.cari.length == 0" class="pb-0">
        <h1 class="text-center">Data tidak ada!</h1>
      </div>
      <div v-if="this.cari.length >= 1" class="grid grid-cols-3 grid-rows-auto gap-3"  :style="{backgroundImage: 'url(../src/assets/bg5.jpg)'}">
        <div class="filtered-list" v-for="l in cari" :key="l">
          <div class="mx-2 mb-auto rounded-b-full rounded-t-full bg-white overflow-hidden shadow-lg p-5 border border-purple-500 w-6xl  pt-4 pb-4">
            <a>
              <img class="w-full p-4" v-bind:src="l.thumbnailUrl" alt="Sunset in the mountains">
              <a class="px-auto text-center py-4" v-on:click="removeElement(key)">
                <div class="font-bold text-base sm:text-lg md:text-xl lg:text-2xl xl:text-3xl mb-2">{{l.title}}</div>
              </a>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SelectedItem',
  props: ["cari", "search"],
    methods: {
      check() {
        console.log(this.search)
      },
      removeElement: function (index) {
        this.list.splice(index, 1);
      }
    }
}
</script>

<style src="../assets/css/styles.css"></style>