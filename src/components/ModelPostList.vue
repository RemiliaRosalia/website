<template>
    <h1>{{ activeTag }} 3D Models</h1> 
    <div class="postList">
        <div class="tagArea">
            <div class="active">
            </div>
            <button v-bind:class="getClass('')" @click="activeTag=''">All</button>
            <button v-bind:class="getClass('2025')" @click="activeTag='2025'">2025</button>
            <button v-bind:class="getClass('2024')" @click="activeTag='2024'">2024</button>
            <button v-bind:class="getClass('2023')" @click="activeTag='2023'">2023</button>
        </div>
        <div class="ModelPosts">
            <div v-for="post in posts" :key="post.id" class="ModelBG">
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
import SinglePost from './ModelSinglePost.vue'
import { ref } from 'vue'
import { useRoute } from 'vue-router';
export default {
    props: ['posts'],
    components: {SinglePost},
    // beforeMount()
    // {
    // //   const urlParam = 2024
    // //   searchTag(urlParam)
    // },
    setup(props)
    {
//        onMounted(() =>console.log('component mounted'))
        const startingTag = useRoute().params.year
        // if(startingTag.value!= '2023' || startingTag.value !='2024')
        // {
        //   startingTag.value=''
        // }
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
                        //console.log(props.posts[realId]);
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
        activeTag.value=startingTag
        //console.log(route.params.year)
        return {activeTag,searchTag, setActiveTag, getClass}
    },

}
</script>

<style>
h1
{
    margin:auto;
    margin-top:0%;
    padding-top:0;
}
.tagArea
  {
    text-align: center;
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
.ModelPosts
  {
    text-align: center;
    /* border: 2px solid black;  */
    display:flex;
    flex-wrap: wrap;
    justify-content: center;
    grid-area: [posts];
    margin-left: 5%;
    margin-right: 5%;
  }
  .ModelPost
  {
    border: .2em solid #1b4375;
    background-color: #6baeff;
    /* background-color: #619ff0; */
    width: 20em;
    height: 20em;
    font-size: .85em;
    -webkit-transition: all .6s ease;
       -moz-transition: all .6s ease;
        -ms-transition: all .6s ease;
         -o-transition: all .6s ease;
            transition: all .6s ease;
  }
  .ModelPost:hover
  {
    width:30em;
    height:30em;
    vertical-align: middle;
  }

  .ModelPost h3
  {
    line-height: 1;
    margin-top:.25em
  }
  .ModelPost img
  {
    width:85%;
    height:85%;
    object-fit:contain;
    /* margin:0%; */
  }
  .ModelPost p
  {
    /* margin:2%; */
    margin-top:0%;
    margin-bottom:0%;
    font-weight: bold;
  }
  .ModelBG
  {
    background-color: #1b4375;
  }
  /* .tagContainer
  {
    color:rgb(34, 19, 255);
    font-weight: 425;
    margin-left: 2.5%;
    margin-right: 2.5%;
    font-size:small;
  } */
  
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