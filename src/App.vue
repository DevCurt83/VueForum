<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <PageHome/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import PageHome from '@/components/PageHome'

export default {
  name: 'App',
  components: {
    HelloWorld,
    PageHome     // PageHome: PageHome could be written like this - but we have made use of the ES6 object shortcut 
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
