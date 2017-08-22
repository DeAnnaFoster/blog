<template>
  <div>
    <h1>Create {{ title }}</h1>
  </div>
</template>

<script>
  export default {
    data(){
      return {
        title: this.$route.params.Title
      }
    },
    mounted(){
      console.log('ABOUT IS READY')
      console.log("WHAT IS THIS?", this.$route.params.Title)
    }
  }
</script>

<style></style>