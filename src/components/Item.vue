<template>
  <div class="h-100 w-full flex items-center justify-center font-sans">
    <div class="border border-white-500 w-full bg-blue-500 shadow-md rounded pt-6 pb-8 px-5">
      <h3 class="text-center font-bold mb-5 text-4xl text-black bg-blue-300">List Item</h3>
      <div class="grid grid-cols-3 grid-rows-3 gap-4"  :style="{backgroundImage: 'url(../src/assets/bg5.jpg)'}">
        <div v-for="f in this.data" :key="f">
          <div class="mx-2 mb-auto rounded-b-full rounded-t-full bg-white overflow-hidden shadow-lg p-5 border border-purple-500 w-6xl  pt-4 pb-4">
            <a v-bind:href="f.url" target="_blank">
              <img class="w-full p-4" v-bind:src="f.thumbnailUrl" alt="Sunset in the mountains">
              <div class="px-auto text-center py-4">
                <div class="font-bold text-base sm:text-lg md:text-xl lg:text-2xl xl:text-3xl mb-2">{{f.title}}</div>
              </div>
            </a>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Item',
  props: ["data"]
}
</script>

<style src="../assets/css/styles.css"></style>