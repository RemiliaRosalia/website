<template>
    <div class="Portfolio">
      <div class="List">
        <!--div v-if ="error"> {{ error }}</div-->
        <div v-if="posts.length">
          <PostList :posts="posts"/>
        </div>
      <!--div v-else>Loading...</div-->
      </div>
    </div>
      
  </template>
  
  <script>

  import PostList from'../components/PostList.vue'
  //automatically knows its a js file
  import postData from '../assets/db.json'


  export default {
    name: 'Portfolio',
    components: { PostList},
    setup() 
    {
      //runs first
      //const { posts, error, load} = getPosts()
      //load()
      const posts = postData.posts;
      console.log(posts.length);
      return{posts}
      //return { posts, error}
    },
    created()
    {

    },
    mounted()
    {

    }
  }
  </script>

  <style>
  .Portfolio
  {
    /* display:grid;
    grid-template-areas:
    'header header header header header header'
    'posts posts posts posts posts sidebar'
    'posts posts posts posts posts sidebar'
    'footer footer footer footer footer footer'; */
    padding-bottom:10%;
  }
  
  </style>
  