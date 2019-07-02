<template>
  <div id="app">
    <navbar></navbar>
    <router-view/>
    <my-footer></my-footer>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue';
import MyFooter from '@/components/MyFooter.vue';

export default {
  components: {
    Navbar,
    MyFooter,
  },
};
</script>


<style>
@tailwind base;
@tailwind components;
@tailwind utilities;

html {
  background: linear-gradient(to bottom right, #024A74, #650274);
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;
}

</style>
