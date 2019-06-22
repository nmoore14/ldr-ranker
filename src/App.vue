<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>

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
