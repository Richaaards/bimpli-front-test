<template>
  <div id="app" class="w-full">
      <restaurants-list />    
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import RestaurantsList from './pages/RestaurantsList'

export default {
  name: 'App',
  components: {
    // HelloWorld
    RestaurantsList,
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
