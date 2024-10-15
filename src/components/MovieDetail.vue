<script setup>
import movies from '@/movies.json'

// import { defineProps } from 'vue';
defineProps({ movie: Object })
</script>

<template>
  <div v-if="movie" class="z-40 text-white w-[53%] h-[50%] pt-20">    
    <div class="text-6xl font-semibold">{{movie.name}}</div>
    <div class="flex items-center text-lg pt-4">
    <div>{{ movie.year }}</div>

    <div class="relative">
      <span class="absolute left-[2px] -top-[26px] text-5xl">.</span>
      <span class="pl-4">{{ movie.genre.one }}</span>  
    </div>
    <div class="relative">
      <span class="absolute left-[2px] -top-[26px] text-5xl">.</span>
      <span class="pl-4">{{ movie.genre.two }}</span>  
    </div>
    <div class="relative">
      <span class="absolute left-[2px] -top-[26px] text-5xl">.</span>
      <span class="pl-4">{{ movie.genre.three }}</span>  
    </div>
  </div>
    <div class="text-2xl pt-6"> {{ movie.description }}</div>
  </div>
</template>

