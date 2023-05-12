<script setup>
// Passed-through data
defineProps({
  data: {}
})

// Local Data
const message = "Hello" 

</script>

<template>
  <div class="flex flex-col items-center gap-x-6">
    <p>{{ message }}</p>
    <img class="h-32 w-32 rounded-full" :src="data.imageUrl" alt="" />
    <div class="mx-auto">
      <h3 class="text-base font-semibold tracking-tight text-gray-900">{{ data.name }}</h3>
      <p class="text-sm font-semibold text-indigo-600">{{ data.role }}</p>
    </div>
  </div>
</template>

<style scoped>

</style>
