<script setup>
defineProps({
  data: {}
})

const message = "Hello"
</script>

<template>
  <div class="flex flex-row items-center gap-x-6">
    <img class="h-32 w-32 rounded-full" :src="data.imageUrl" alt="" />
    <div>
      <h3 class="text-base font-semibold leading-7 tracking-tight text-gray-900">{{ data.name }}</h3>
      <p class="text-sm font-semibold leading-6 text-indigo-600">{{ data.role }}</p>
    </div>
  </div>
</template>

<style scoped>

</style>