<template>
    <div class="smallPost">
      <router-link :to="{path: '/project/' + post.url}">
          <img :src="post.icon"  class="smallPostImg">
          <h3 width="100%" class="smallPostTitle"> {{ post.title }}</h3>
      </router-link>
    </div>
  </template>
  
  <script>
  export default 
  {
      props: ['post'],
      setup(props)
      {
          const getIcon = ()=>
          {
            console.log(props.post.icon + "  |  ../assets/JNJFotG.png");
            return "../assets/JNJFotG.png"
          }
         return {getIcon}
      }
  }
  </script>
  
  <style>
  .smallPost
  {
    border: .2em solid  #1b4375;
    background-color: #6baeff;
    width: 17.5em;
    height: 14.5em;
  
  }
  .smallPostTitle
  {
    font-size: 1em;
    margin: 0%;
  }
  .smallPostImg
  {
    margin-top:2.5%;
    width:95%;
    height:70%;
    object-fit:contain;
  }
  </style>