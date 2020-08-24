<template>
  <div class="h-100 w-full flex items-center justify-center font-sans">
    <div class="border border-white-500 w-full bg-blue-500 shadow-md rounded pt-6 pb-8 px-5">
      <div class="grid grid-cols-3 grid-rows-auto gap-3"  :style="{backgroundImage: 'url(../src/assets/bg5.jpg)'}">
        <div class="filtered-list" v-for="l in cari" :key="l">
          <div class="max-w-sm rounded overflow-hidden shadow-lg">
            <a v-bind:href="l.url">
              <img class="w-full" v-bind:src="l.thumbnailUrl" alt="Sunset in the mountains">
              <div class="px-6 py-4">
                <div class="font-bold text-xl mb-2">Title of image id {{l.title}}</div>
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
  name: 'SelectedItem',
  props: ["cari", "search"],
    methods: {
        checkSearch() {
          console.log(this.search)
        }
    }
}
</script>

<style src="../assets/css/styles.css"></style>