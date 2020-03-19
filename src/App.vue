<template>
  <div id="app">
    <HomePage msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
import HomePage from "./components/HomePage.vue";

export default {
  name: "App",
  components: {
    HomePage
  }
};
</script>

<style>
html,
body {
  height: 100%;
  width: 100%;
  padding: 0;
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  width: 100%;
  height: 100%;
}
* {
  box-sizing: border-box;
}
</style>
