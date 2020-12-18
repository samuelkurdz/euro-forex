<template>
  <div class="card bg-white pt-2 shadow-xs hover:shadow-xl rounded-lg overflow-hidden my-3">
    <div class="bg-contain bg-no-repeat bg-center h-32 p-4"
         :style="{ backgroundImage: `url(${image})` }">
    </div>
    <div class="px-4 py-2 border-t mt-2">
      <p class="text-xl text-gray-900 text-center">{{title}}</p>
    </div>
    <div class="px-4 pt-3 pb-4 border-t border-gray-300">
      <span class="text-center">
        {{text}}
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    image: String,
    title: String,
    text: String,
  }
}
</script>

<style scoped>
.card {
  width: 19rem;
  height: 23.5rem;
  max-width: 19rem;
}
</style>
