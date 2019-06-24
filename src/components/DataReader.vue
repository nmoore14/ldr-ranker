<template>
  <div
    class="flex flex-row flex-wrap"
  >
    <div
      v-for="(show, index) in ldr_data.ldr.shows"
      :key="index"
      class="max-w-sm rounded shadow-lg m-4 card"
    >
      <img class="w-full" :src="show.imageUrl" :alt="show.title + ' poster image'">
      <div class="px-6 py-4">
        <h1 class="font-sans font-light text-2xl">{{ show.title }}</h1>
        <p class="text-gray-700 text-base h-64">
          {{ show.description }}
        </p>
      </div>
      <div>
        <h3 class="font-sans font-light text-center text-3xl">
          <span class="text-green-800">{{ show.up }}</span>&nbsp;/&nbsp;
          <span class="text-red-700">{{ show.down }}</span>
        </h3>
        <p class="font-sans font-light text-center text-xl -mt-3 mb-4">Vote Rating</p>
      </div>
      <div
        class="flex flex-row w-full justify-center mb-4"
      >
        <button class="bg-teal-500 hover:bg-teal-700 text-white font-bold py-2 px-4">
          Like
        </button>
        <button class="bg-red-400 hover:bg-red-700 text-white font-bold py-2 px-4">
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
