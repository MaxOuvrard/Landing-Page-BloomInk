<script setup lang="ts">
defineProps<{
  title: string
  description: string
  image: string
}>()
</script>

<template>
  <div class="rounded-4xl overflow-hidden glass">
    <img :src="image" class="w-full" alt="">
    <div class="flex flex-col gap-3 px-10 py-7">
      <h3 class="text-xl font-bold">{{ title }}</h3>
      <p>{{ description }}</p>
    </div>
  </div>
</template>

<style scoped>

</style>