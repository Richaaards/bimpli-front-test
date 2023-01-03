<template>
  <div id="app" class="w-full">
      <!-- <restaurants-list />
      <restaurant-info /> -->
      <router-view></router-view>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import RestaurantsList from './pages/RestaurantsList'
// import RestaurantInfo from './pages/RestaurantInfo'

export default {
  name: 'App',
  components: {
    // HelloWorld
    // RestaurantsList,
    // RestaurantInfo,
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
