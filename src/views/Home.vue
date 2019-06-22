<template>
  <div
    class="container mx-auto"
  >
    <data-reader></data-reader>
  </div>
</template>

<script>
// @ is an alias to /src
import DataReader from '@/components/DataReader.vue';

export default {
  name: 'home',
  components: {
    DataReader,
  },
};
</script>
