<template>
  <div id="app">
    <img alt="Vue logo" width=50 src="./assets/logo.png">
    <PaginaPrincipal />
  </div>
</template>

<script>
import PaginaPrincipal from './components/HelloWorld.vue'
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

export default {
  name: 'App',
  components: {
    PaginaPrincipal
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
