<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <button id="add-count" v-on:click="eventBus.emit({name: 'add-count', data: true})">Counter +1</button>
    <p>created by {{ author }}</p>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  props: {
    eventBus: Object,
    author: String,
  },
  components: {
    HelloWorld
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

#add-count {
  border: 0;
  padding: 0.7rem;
  background-color: #2c3e50;
  color: white

}
</style>
