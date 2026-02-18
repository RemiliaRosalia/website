<template>
<!-- <title>{{TabTitle}}</title> -->
<div class="home">
    <!--div v-if="errorFeat"> {{ errorFeat }} </div-->
    <div class="featuredBorder container">
      <router-link to="/project/Journeys_and_Jazz_The_Fruits_of_the_Gods" class="noHoverColor">
        <div class="featured row" v-if="postFeat">
          <transition>
            <img src="..\assets\JNJFotG.png" class="featuredImg leftCol">
          </transition>
      <div class="featuredText col">
          <h1 class= featuredTitle><u>{{ "Journeys and Jazz: The Fruits of the Gods" }}</u></h1>
          <h2 class="featuredTitle">
            <u>Part 3 Released!</u>
          </h2>
          <div class="featuredSmallImg" @mouseleave="changeFeatImg('https://github.com/RemiliaRosalia/website/blob/main/dist/img/JNJFotG.5cb790a4.png?raw=true')">
            <img src="../assets/JNJ/Colosseum.png" width="25%" @mouseover="changeFeatImg('https://raw.githubusercontent.com/RemiliaRosalia/website/refs/heads/main/dist/img/Colosseum.38b73c1f.png')" >
            <img src="../assets/JNJ/DataKuzgar.png" width="25%" @mouseover="changeFeatImg('https://raw.githubusercontent.com/RemiliaRosalia/website/refs/heads/main/dist/img/DataKuzgar.8b8f3a82.png')">
            <img src="../assets/JNJ/OldMan.png" width="25%" @mouseover="changeFeatImg('https://github.com/RemiliaRosalia/website/blob/gh-pages/img/OldMan.873f7bfe.png?raw=true')">
          </div>

            <p>This new update to Journeys and Jazz: The Fruits of the Gods
          adds the city of Alicia and around 2-3 hours of content.
          Play and explore what Alicia has to offer such as fighting in the colloseum and entering hot dog eating contests!
            </p>

                <!-- <u>Click here to learn more!</u>  -->
      </div>
    </div>
      </router-link>
    </div>

    <div>
      <!--div v-if ="error"> {{ error }}</div-->
      <div v-if="posts.length">
        <HomePostList :posts="posts"/>
      </div>
      <!--div v-else>Loading...</div-->
    </div>

  </div>


</template>

<script>
  import HomePostList from'../components/HomePostList.vue'
  import postData from '../assets/db.json'
  import VueScreen from 'vue-screen'
  import TabTitle from '../App.vue'
export default 
{
  name: 'HomeView',
  components: { HomePostList},
  props: ['id'],
  setup() 
    {
      const posts = postData.posts
      //var featuredImg = "https://github.com/RemiliaRosalia/website/blob/gh-pages/img/JNJFotG.5cb790a4.png?raw=true"
      const postFeat = posts[4]
      TabTitle = "Remi"
      const changeFeatImg = (newImg) =>
        {
          var image = document.getElementsByClassName("featuredImg")[0]
          console.log(image)
          image.src = newImg;
        }
      return{posts, postFeat, changeFeatImg, VueScreen, TabTitle}

    },
}
</script>

<style>
.home
{
  padding-bottom: 2.5em;
}
.featured
{
  /* background-color: #609de9; */
  background-color: #6baeff;
  border: .25em solid #ffee00;
  /* border-style:  groove  ridge ridge groove ; */
  align-self: center;
  height:27.5em;
}

.featuredBorder
{
  /* width: 100%; */
  margin: auto;
  margin-top: 2em;
  border: .25em solid #ffa946;
  
 
}
.featuredImg
{
  object-fit:contain;
  /* object-position: center; */
  /* vertical-align:top; */
  /* display: inline-block; */
  height: 25em;
  margin:auto;
  /* margin:auto; */

}
.featuredSmallImg
{
  text-align: center;
  margin-top:.5em;
  margin-bottom:.5em;
}
.featuredSmallImg img
{
  margin-left:2.5%;
  opacity:70%;
  margin-right:2.5%;
  -webkit-transition: all .4s ease;
       -moz-transition: all .4s ease;
        -ms-transition: all .4s ease;
         -o-transition: all .4s ease;
            transition: all .4s ease;
}

.featuredSmallImg img:hover
{
opacity: 100%;
}
.featuredText
{
  /* background-color: aquamarine; */
  display: inline-block;
  margin:auto;
  width:66%;
}
.featured h1 
{
  margin: auto auto .25em auto;
  line-height: 125%;
}
.featuredText h2
{
  text-align: center;
  margin:0em auto 1.25em auto;

}
.featuredText p
{
  margin-top:.5em;
  margin-left:10%;
  margin-right:10%;
  font-size: large;
  display: inline-block;
  vertical-align: middle;
  line-height: normal;
}
.featuredTitle
{
  /* text-align: center; */
  margin-top:0%;
  padding-top:0%;
}

h3
{
  margin-left: 2%;
}
.Container
{
  display: flex;
  flex-flow: row wrap;
  justify-content: space-around;
  padding: 0;
  margin: 0;
  list-style: none;
}
.leftCol
{
  flex: 0 0 35%;
  max-width: 35%;
}

@media (max-width:900px)
{
  .featured
{
  text-align: center;
}

.featuredImg
{
  object-fit:contain;
  height: 25em;
  margin:auto;

}
.featuredSmallImg
{
  text-align: center;
  margin-top:.5em;
  margin-bottom:.5em;
}
.featuredSmallImg img
{
  margin-left:2.5%;
  opacity:70%;
  margin-right:2.5%;
  -webkit-transition: all .4s ease;
       -moz-transition: all .4s ease;
        -ms-transition: all .4s ease;
         -o-transition: all .4s ease;
            transition: all .4s ease;
}

.featuredSmallImg img:hover
{
opacity: 100%;
}
.featuredText
{
  /* background-color: aquamarine; */
  display: inline-block;
  margin:auto;
}
.featured h1 
{
  font-size:x-large;
}
.featuredText h2
{
  font-size:larger;
}
.featuredText p
{
  margin-left:0%;
  margin-right:0%;
  font-size: medium;
}
.container
{
  max-width: 75%;
}
}

@media (max-width:1250px)
{

.featuredText p
{
  margin-left:0%;
  margin-right:0%;
  font-size: medium;
}
  .container
{
  max-width: 80%;
}
.HomePosts
  {
    justify-content: center;
  }
}
</style>
