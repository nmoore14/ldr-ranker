<template>
  <div>
      <div
        v-for="(show, index) in ldr_data.ldr.shows"
        :key="index"
        class="showContainer"
      >
        <h2>{{ show.title }}</h2>
        <img :src="show.imageUrl" :alt="show.title + ' poster image'">
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
  .showContainer {
    background-color: #e6e6e6;
  }
</style>
