<template>
    <div class="CV">
      <div>
        <h1>Work Experience</h1>
        <div>
          <h2>Digital Personal Shopper | Walmart | 11/2024 – Present</h2>
          <div class="bullets">
          <p>● Pick, Stage, and Dispense customers’ orders.</p>
          <p>● Stay in constant communication with coworkers on where help was needed most.</p>
          <p>● Aid in-store customers</p>
          </div>
        </div>

        <div>
          <h2>Volunteer Game Designer | P[1] Games | 07/2024 – 09/2024</h2>
          <div class="bullets">
            <h4>Jira, Miro, Discord</h4>
          <p>● Worked with a small team on a 2D platformer as one of two game designers.</p>
          <p>● Designed puzzles, mechanics, enemies, and levels for a 2D platformer prototype.</p>
          <p>● Worked with programmers and artists to design mechanics within their scope.</p>
          <p>● Observed and playtested to see what mechanics work and which could be improved and how to improve them.</p>
          </div>
        </div>

        <div>
          <h2>Unity Intern | The Commons XR | 03/2024 – 06/2024</h2>
          <div class="bullets">
            <h4>Unity, C#, Github, Slack</h4>
          <p>● Aided in the development of an XR muliplayer software for use in education and mental health environments.</p>
          <p>● Designed a new 3D area for use in therapy and classrooms based on a outdoors camp scene.</p>
          <p>● Fixed bugs such as players going out of bounds, flickering lighting, and desyncing between different users.</p>
          <p>● Collaborated with teammates to test our changes together and exchange critiques. </p>
          <p>● Participated in system tests to consumer use in order to explore potential issues in mine and other’s work.</p>
          </div>
        </div>
        <div>
            <h2>Peer Tutor | TCNJ Tutoring Center | 09/2021 - 06/2024</h2>
            <div class="bullets">
              <h4>Zoom, p5.js, JavaScript, html</h4>
            <p>● Aided fellow students with their Interactive Multimedia assignments.</p>
            <p>● Typically focused on debugging JavaScript code.</p>
            <p>● Work involved reviewing code and guiding the student towards the solution without stating it.</p>
            <p>● Sessions lasted one hour and could be done once a week.</p>
          </div>

        </div>
      </div>
      <div>
        <h1>Personal Experience</h1>
        <div>
          <router-link to="/project/Journeys_and_Jazz_The_Fruits_of_the_Gods"><h2>Journeys and Jazz: The Fruits of the Gods | Solo Developer | 09/2022 – Present</h2></router-link>
          <div class="bullets">
            <h4>RPG Maker MZ, JavaScript, Clip Studio Paint, Photoshop</h4>
          <p>● Converted multiple sessions of a Tabletop RPG campaign into a playable turnbased RPG game.</p>
          <p>● Carefully balancesd the four playable characters to fill their own useful niches.</p>
          <p>● Created plugins to modify the game engine to alter mechanics and create new ones.</p>
          <p>● Designed various towns, dungeons, puzzles, and NPCs, along with art for the playable cast and many enemies.</p>
          </div>

        </div>
        <div>
          <router-link to="/project/Gift_of_Pain"><h2>Gift of Pain | Lead 3D Artist & Assistant Programer | 09/2024 – Present</h2></router-link>
          <div class="bullets">
            <h4>Blender, Unity, C#, Photoshop, Github</h4>
          <p>● Worked with 3 others to create a 3D Christmas themed Third-Person Action Game.</p>
          <p>● In charge of creating the main character and many environmental assets.</p>
          <p>● Created animations to play in game and concurrently through animation layers.</p>
          <p>● Aided with miscellaneous programming tasks such as menu scripts and action scripts.</p>
          </div>

        </div>
        <div>
        <router-link to="/project/Royal_Flush"><h2>Royal Flush | Lead Programmer | 01/2022 – 05/2022</h2></router-link>
        <div class="bullets">
          <h4>Unity, C#</h4>
          <p>● Worked with 4 others to create a Unity game prototype under the supervision of a professor.</p>
          <p>● Developed a physical prototype to test gameplay mechanics early on.</p>
          <p>● In charge of balancing combat and creating combat mechanics such as skills.</p> 
          </div>

        </div>
      </div>
    </div>
  </template>
<style>
.CV
{
  padding-bottom: 7.5em;
}
h1
{
  text-align: center;
  
}
h2
{
  margin-left: 15%;
}
h4
{
  margin-left: 2%;
}
p
{
  margin-left: 2%;
  margin-bottom: 0;
}
.bullets
{
  margin-left:8%;
  border-left:.5em solid #0053b9;
}
@media (max-width:900px)
{
  h2
  {
    text-align: center;
    margin:5% auto -1% auto;
  }
  .bullets
{
  margin-left:5%;
}
}
</style>
  