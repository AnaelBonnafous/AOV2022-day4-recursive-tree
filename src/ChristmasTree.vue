<template>
  <div>
    <div>
      <ChristmasTree v-if="size > 1" :size="size - 1" />

      <div class="flex flex-row justify-center">
        <div v-for="i in size" class="relative rounded-full bg-green w-16 h-16 -m-2 flex justify-center items-center" />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
withDefaults(
  defineProps<{
    size: number
  }>(),
  {
    size: 1,
  }
)
</script>
