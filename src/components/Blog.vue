<template>
  <div>
    <h1>Blog: {{ title }}</h1>
    <h3>Post: {{ body }}</h3>
  </div>
</template>

<script>
  export default {
    data(){
      return {
        title: this.$route.params.blogTitle,
        body: this.$route.params.blogBody
      }
    },
    mounted(){
      // console.log('ABOUT IS READY')
      // console.log("WHAT IS THIS?", this.$route.params.blogTitle)
    }
  }
</script>

<style></style>