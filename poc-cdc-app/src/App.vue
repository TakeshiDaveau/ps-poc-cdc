<template>
  <div id="app">
    <my-hello-world></my-hello-world>
  </div>
</template>

<script>
import Vue from 'vue';
// import HelloWorld from './components/HelloWorld.vue'
import * as zoid from 'zoid/dist/zoid.frameworks.js'

const MyHelloWorld = zoid.create({
  tag: 'my-hellow-world',
  url: 'http://localhost:8089',
  dimensions: {
    width: '500px',
    height: '700px'
  }
}).driver('vue', Vue);

export default {
  name: 'App',
  components: {
    'my-hello-world': MyHelloWorld
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
