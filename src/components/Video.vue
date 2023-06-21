<template>
  <div class="hover:bg-gray-800 md:rounded-2xl cursor-pointer">
    <img class="md:rounded-2xl " :src="props.video.thumbnail" alt="Thumbnail" />
    <div class="flex items-start p-2 gap-4">
      <img class="rounded-full w-12 h-12" :src="props.video.icon" alt="Channel icon" />
      <div class="flex flex-col">
        <p class="font-bold">{{ props.video.title }}</p>
        <p class="text-gray-400">{{ props.video.channel }}</p>
        <div class="flex gap-4">
          <p class="text-gray-400">{{ props.video.views }} views</p>
          <p class="text-gray-400">{{ props.video.publishedAt }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import type { Video } from '../videos'

const props = defineProps<{ video: Video }>()
</script>

<style></style>
