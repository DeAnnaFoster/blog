<template>
  <div>
    <h1>Blogs in VUE</h1>

    <div class="create">
       <form @submit.prevent="createBlog()">
        <input type="text" v-model="blog.title" placeholder="Title">
        <wysiwyg v-model="blog.body" />
        <button class="btn btn-primary" type="submit">Submit</button>
      </form> 
    </div>

    <!-- <div>
      <button @click="createBlog">Create New Blog</button>
    </div> -->
 
     <ul>
      <li v-for="blog in blogs">
        <router-link :to="{name: 'Blog', params: { blogId: blog._id } }">{{blog.title}} : {{blog._id}}</router-link>
      </li>
    </ul>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        blog:{
          title:'',
          body:''
        }
        // blogs:[{
        //   title: '103 Ways to Sink Your Ship',
        //   body: 'Pull the plug and more'
        // },{
        //   title: '51 Ways to Float Your Boat',
        //   body: 'Start with a float'
        // }]
        //blogs: store.state.blogs
      }
    },
    computed: {
      blogs() {
        return this.$store.state.blogs
      }
    },
    // beforeCreate() {
    //   //store.getBlogs();
    // },

    methods: {
      createBlog() {
        var createdBlog = this.blog;
        this.$store.dispatch("createBlog", createdBlog)
      }
    },

    mounted() {
      this.$store.dispatch('getBlogs')
    }

  }

</script>

<style></style>