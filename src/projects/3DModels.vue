<template>
    <div class="projectPage">
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
    import PostList from'../components/ModelPostList.vue'
    import postData from '../assets/Models_db.json'
    export default {
    name: '3DModels2024',
    components: { PostList},
    setup() 
    {
      const posts = postData.posts;
      console.log(posts.length);
      return{posts}
    },
    created()
    {

    },
    mounted()
    {

    }
  }
  </script>
  