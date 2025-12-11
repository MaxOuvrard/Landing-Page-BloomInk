<script setup lang="ts">
defineProps<{
  title: string
  description: string
}>()
</script>

<template>
  <details class="group mb-4 rounded-xl px-7 py-4 bg-slate-100 w-200 border-1">
    <summary class="cursor-pointer text-lg flex justify-between items-center">
      {{ title }}
      <span class="transition-transform group-open:rotate-180">
        <img src="/plus-icon.svg" alt="">
      </span>
    </summary>

    <div class="mt-3 text-gray-600 text-wrap">
      {{ description }}
    </div>
  </details>
</template>

<style scoped>

</style>