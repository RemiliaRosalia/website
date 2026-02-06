<template>
    <h1>{{ activeTag }} Projects</h1>
    <div class="postList">
        <div class="tagArea">
            <div class="active">
            </div>
            <button v-bind:class="getClass('')" @click="activeTag=''">All</button>
            <button v-bind:class="getClass('Game')" @click="activeTag='Game'">Games</button>
            <button v-bind:class="getClass('3D')" @click="setActiveTag('3D')">3D</button>
            <button v-bind:class="getClass('Programming')" @click="activeTag='Programming'">Programming</button>
            <button v-bind:class="getClass('Game Design')" @click="activeTag='Game Design'">Game Design</button>
        </div>
        <div class="posts">
            <div v-for="post in posts" :key="post.id">
                <div v-if="activeTag==''">
                    <SinglePost :post="post" />
                </div>
                <div v-else-if="searchTag(activeTag, post.id)">
                    <SinglePost :post="post"/>
                </div>
            </div>
        </div>

    </div>
</template>

<script>
import SinglePost from './SinglePost.vue'
import { ref } from 'vue'
export default {
    props: ['posts'],
    components: {SinglePost},
    setup(props)
    {
//        onMounted(() =>console.log('component mounted'))
        const activeTag = ref('')
        const searchTag = (tag, postId)=>
        {
            //for(var i=0;i<props.posts.length;i++)
            //{
                var realId = props.posts.length - postId;
                for(var j=0;j<props.posts[realId].tags.length;j++)
                {
                    if(props.posts[realId].tags[j].match(tag))
                    {
                        console.log(props.posts[realId]);
                        return true;
                    }   
                }
            //}
        }
        const setActiveTag = (tag) =>
        {
        activeTag.value=tag;
        }
        const getClass = (name) =>
        {
            if(activeTag.value==name)
                return "activeTag"
            else   
                return "notActiveTag"
        }
        return {activeTag,searchTag, setActiveTag, getClass}
    },

}
</script>

<style>
.tagArea
  {
    grid-area: [sidebar];
    /* float:right; 
    width:17.5%;*/
    text-align: center;
    padding-bottom:.5em;
  }
  .tagArea button
  {
    font-size: large;
    margin:0em 1em .5em 1em;
    border:none;
    background-color: transparent;
    /* font-weight: 500; */
    text-decoration: underline;
  }
  .notActiveTag:hover
  {
    color:#0072ff;
  }
  .tagArea button:active
  {
    color:#ee7700;
  }
  .activeTag
    {
        color:#ee7700;
        font-weight: 600;

    }
  .active
  {
    width:100%;
  }
  .active button
  {
    text-align: center;
    align-content: center;
    align-self: center;
  }
  .posts
  {
    text-align: center;
    /* border: 2px solid black;  */
    display:flex;
    flex-wrap: wrap;
    margin-left: 2.5%;
    margin-right: 2.5%;
    justify-content: center;
    grid-area: [posts];
  }
  .post
  {
    border: .2em solid #1b4375;
    background-color: #6baeff;
    /* background-color: #619ff0; */
    width: 26.5em;
    height: 21.25em;
    font-size: .85em;
  }

  .post h3
  {
    line-height: 1;
    margin:3%;
    margin-top:1%;
  }
  .post img
  {
    width:75%;
    height:57.5%;
    object-fit:contain;
    margin:0%;
  }
  .post p
  {
    margin:2%;
    margin-top:0%;
    margin-bottom:0%;
    font-weight: bold;
  }

  .tagContainer
  {
    /* color:rgb(11, 71, 201); */
    color:rgb(34, 19, 255);
    font-weight: 425;
    margin-left: 2.5%;
    margin-right: 2.5%;
    font-size:small;
  }
  @media (max-width:768px)
{
  .tagArea button
  {
    font-size: large;
    margin:0em .25em .5em .25em;
    border:none;
    background-color: transparent;
    /* font-weight: 500; */
    text-decoration: underline;
  }
}
</style>