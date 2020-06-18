<template>
<!--  <img src="./assets/logo.png">-->
  <div id="app">
<!--    <div id="nav">-->
<!--      <router-link to="/">Hello</router-link>-->
<!--      <router-link to="/about">About</router-link>-->
<!--    </div>-->
    <router-view/>
  </div>
</template>

<script>
  export default {
    name: 'App'
  }
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: left;
    color: #2c3e50;
    margin-top: 20px;
    margin-left: 20px;
  }
  /*#nav {*/
  /*  padding: 30px;*/
  /*}*/
</style>
