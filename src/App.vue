<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <Hola />
    <Drawner />
    <Carruzel />
    <InputStates />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Hola from './components/mau.vue'
import Carruzel from './components/Carruzel.vue'
import InputStates from './components/InputState.vue'
import Drawner from './components/Drawner.vue'
export default {
  name: 'App',
  components: {
    HelloWorld, Hola, Carruzel,InputStates,Drawner
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
