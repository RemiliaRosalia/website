<template>

  <transition>
    <div class="ModelPost" @click="openBigPreview(post)" >
        <h3> {{ post.title }}</h3>
        <img :src="post.icon" v-if="!showPreview">
        <img v-else src="https://cdn.bsky.app/img/feed_fullsize/plain/did:plc:ps2uvxlt6amozhvzgnkmlt5c/bafkreief44m5em3hx5thavar7mmmywvq22shuj7oflckol26e45es5n7xe@jpeg"> 
    </div>
  </transition>
  </template>
  
  <script>
  import { computed } from 'vue';
  export default 
  {
      props: ['post'],
      setup(props)
      {
          var previewImg = '';
          var showPreview = false;
          const getIcon = (imgUrl)=>
          {
            let C= '../assets/3DModels/' + imgUrl;
            let A = new URL("../assets/3DModels/Donut3.gif", import.meta.url)
            let B = new URL ("../assets/3DModels/" + imgUrl, import.meta.url)
            if(imgUrl == "Donut3.gif")
            {
              console.log(A==B)
              console.log(A)
              console.log(B)
            }
            //return new URL("../assets/3DModels/Donut3.gif", import.meta.url)
            return B
          }
          const openBigPreview = (post)=>
          {
            previewImg = post.icon;
            showPreview= true;
            console.log("HIIIII")
          }
          return {getIcon, openBigPreview,previewImg,showPreview}
      }
  }
  </script>
  
  <style>
  </style>