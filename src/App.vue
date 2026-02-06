<template>
  <head>
    <link rel="icon" href="./assets/RemiliaRosaliaIcon_256.png">
  </head>

  <body>
    <nav class="header">
    <div class="logo">
      <router-link to="/" ><img src='./assets/logo.jpg' width="200px"> </router-link>   
    </div>
    <div class="navLinks">
      <router-link to="/" class="navRight">Home</router-link>&emsp;&emsp;
      <router-link to="/portfolio" class="navRight">Portfolio</router-link>&emsp;&emsp;
      <router-link to="/cv" class="navRight">CV</router-link>  &emsp;&emsp;
      <router-link to="/about" class="navRight">About</router-link>
      </div>
  </nav>
  </body>
  <router-view/>
  <!-- <h1>FLEX TEST</h1>
  <ul class="container">
    <li class="item">YO</li>
    <li class="item">YO</li>
    <li class="item">YO</li>
    <li class="item">YO</li>
  </ul> -->
</template>

<script>

export default
{

}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Permanent+Marker&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Rakkas&display=swap');
#app 
{
  font-family: Poppins,Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #182735;
  background-image: linear-gradient(#cde1ff, rgb(147, 185, 255));
  /* background-color: #a1ccff; */
  margin: 0;
  min-height: 100vh;
}

h1
{
  text-align: center;
}
.header
{
  text-align: center;
  margin: 0%;
  width: 100%;
  background-color:#afcdff;
}
.about
{
  text-align: center;
}

nav
{
  margin-top:-0%;
  padding-bottom: 0px;
  font-size: larger;
}
a:visited
{
  color:#182735
}
a:hover
{
  color:#0072ff;
  /* color:#3464ff; */
}
.navLinks
{
  /* background-color: #BCBCBC; */
  padding-bottom: 5px;
  /* padding-top: 0px; */
  /* margin-top: -10px; */
  width: 100%;
  /* border-bottom: 6px solid #0072ff; */
}

.logo
{
  vertical-align: middle;
  text-align: left;
  padding-top: 5px;
  padding-bottom: 0px;
  margin-bottom: -2em;
  padding-left: 30px;
  
}
nav a {
  font-weight: bold;
  color: #2c3e50;
}
body
{
  width: 100%;
  margin: 0%;
}
nav a.router-link-exact-active {
  /* color: #ff8800; */
  color:#ee7700;
}
.projectPage
{
  margin-top:1em;
  margin-left: 10%;
  margin-right: 10%;
  /* background-color: antiquewhite; */
  padding-bottom:3em;
}
.projectPage h1
{
  margin-bottom:0%;
}
.projectPage p
{
  margin-left: 25%;
  margin-right: 25%;
  text-align: center;
}
.projectPage h2
{
  margin-left: 10%;
  margin-top:0%;
  font-size:large;
}
h5
{
  margin-top: 0%;
}
.projectIMG
{
  text-align: center;
}
.projectImages
  {
    text-align: center;
    /* border: 2px solid black;  */
    /* display:flex;
    flex-wrap: wrap; */
    justify-content: center;
    width:90%;
    margin:auto
  }

  .projectImages img
  {
    margin:.25em;
    height: 17.5em;
  }
  .longImg
  {
    text-align: center;
  }
  .longImg img
    {
      height:15em;
      margin:.25em;
    }
.noHoverColor:hover
{
  color: inherit;
}

.col
{
  flex: 0 0 60%;
  max-width: 60%;
}
.container
{
  width: 100%;
  max-width: 65%;
  margin:auto;
}
.row
{
  display: flex;
  flex-wrap: wrap;
  /* width:100% */
}

@media (max-width:900px)
{
  .logo
  {
    margin-bottom: -.5em;
  }
  
}
</style>
