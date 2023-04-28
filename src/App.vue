<template>
  <button v-on:click="show = !show">Menu</button>
  <Transition name="fade">
    <MenuInicio v-show="show" />
  </Transition>
  
  
</template>

<script>
import MenuInicio from './components/MenuInicio.vue';


export default {
  name: 'App',
  components: {
    MenuInicio
  },
  data() {
    return {
      show: false,
    };
  },

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

.fader-leave-active,
.fade-enter-active {
  transition: opacity 0.5s ease;
}

.fade-enter-from,
.fade-leave-to {
  transition: opacity 0;
}
</style>

