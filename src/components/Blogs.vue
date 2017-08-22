<template>
  <div>
    <h1>Blogs in VUE</h1>

    <ul>
      <li v-for="blog in blogs">
        <router-link :to="{name: 'Blog', params: { blogTitle:  blog.title, blogBody: blog.body } }">{{blog.title}}</router-link>
      </li>
    </ul>

  </div>
</template>

<script>
  export default {
    data(){
      return {
        blogs:[{
          title: '103 Ways to Sink Your Ship',
          body: 'Pull the plug and more'
        },{
          title: '51 Ways to Float Your Boat',
          body: 'Start with a float'
        }]
      }
    },
    beforeCreate(){
      console.log("WHAT IS THIS?", this.name)
    },
    mounted(){
      console.log('ABOUT IS READY')
      console.log("WHAT IS THIS?", this.name)
    }
  }
</script>

<style></style>