<template>
  <div id="app">
<!--     <router-link :to="{ name: 'Home' }">Home</router-link>
    <router-link to="/about">About</router-link>
    <router-link to="/coins/ethereum">Ethereum</router-link>
    <router-link to="/coins/bitcoin">Bitcoin</router-link>
    <router-link to="/coins/ripple">Ripple</router-link>
    <router-link to="/coins/tron">Tron</router-link> -->
    <router-link to="/categories">Categories</router-link>
    <router-view></router-view>
    <img src="./assets/th-logo.png">
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  display: flex;
  flex-direction: column;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
img {
  margin: 0 auto;
  padding-top: 25px;
  width: 200px;
}
</style>
