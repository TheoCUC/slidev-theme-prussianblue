<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  props: {
    id: {
      type: Number,
      required: true,
    }
  },
})
</script>

<template>
  <div class="z-90 flex absolute bottom-0 w-full py-8px">
    <span class="flex w-full">
      <div v-for="(item, index) in $slidev.configs.contents" class="text-center flex-auto px-5">
        <div v-if="id-1 == index" class="text-white">{{ item }}</div>
        <div v-else class="text-blue-gray-500">{{ item }}</div>
      </div>
    </span>
  </div>
</template>