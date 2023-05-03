<template>
    <Home first-name = "Linda" last-name = "Chang Tirado"></Home>
</template>

<script>
import Home from "./components/Home.vue";
import { provide } from "vue";

export default {
  name: 'App',
  components: {
    Home
  },
  setup() {
    provide ("username", "Eres un cielo");
  }
  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

