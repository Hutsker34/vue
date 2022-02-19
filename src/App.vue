<template>
  <img alt="Vue logo" src="./assets/лыжник.png">
  <HelloWorld msg="Welcome to Vue.js"/>
  <Todo msg ="Welcom to Todo" img = "https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/1200px-Vue.js_Logo_2.svg.png"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Todo from './components/Todo.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    Todo
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
