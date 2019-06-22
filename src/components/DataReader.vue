<template>
  <div
    class="flex flex-row flex-wrap"
  >
    <div
      v-for="(show, index) in ldr_data.ldr.shows"
      :key="index"
      class="max-w-sm rounded overflow-hidden shadow-lg m-4 card"
    >
      <img class="w-full" :src="show.imageUrl" :alt="show.title + ' poster image'">
      <div class="px-6 py-4">
        <h1 class="font-sans font-light text-2xl">{{ show.title }}</h1>
        <p class="text-gray-700 text-base">
          {{ show.description}}
        </p>
      </div>
      <div>
        <h3 class="font-sans font-light text-center text-3xl">{{ show.totalVotes }}</h3>
        <p class="font-sans font-light text-center text-xl -mt-3">Vote Rating</p>
      </div>
      <div class="inline-flex">
        <button class="bg-gray-300 hover:bg-gray-400 text-gray-800 font-bold py-2 px-4 rounded-l">
          Like
        </button>
        <button class="bg-gray-300 hover:bg-gray-400 text-gray-800 font-bold py-2 px-4 rounded-r">
          Dislike
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import LDR from '@/docs/ldr-rank.json';

export default {
  name: 'DataReader',
  data() {
    return {
      ldr_data: LDR,
    };
  },
};
</script>

<style>
  .card {
    background:#b8b8b8;
    background-size: cover;
    background-repeat: no-repeat;
    background-attachment: fixed;
  }
</style>
