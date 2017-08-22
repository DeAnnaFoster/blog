<template>
  <div id="app">
    <div>
      <!-- THIS IS YOUR NEW <a> -->
      <router-link :to="{name: 'Home'}">Home</router-link>
      <router-link :to="{name: 'Blogs'}">Blogs</router-link>
    </div>
    <hr>
    <router-view></router-view>
    <hr>
    <footer>
      I'm not as think as you drunk I am!
    </footer>
  </div>
</template>

<script>
  export default {
    name: 'app'
  }



</script>

<style>
  /* #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  } */

   @import "~vue-wysiwyg/dist/vueWysiwyg.css";  

  a {
    font-size: 30px;
    color: red;
  }

</style>