<template>
      <div class="projectPage">
        <h1>Journeys And Jazz: The Fruits of the Gods</h1>
        <div class="projectIMG">
          <img src='../assets/JNJFotG.png' height="400em">
          <h5>Tools used: RPG Maker MZ, JavaScript, Photoshop, Clip Studio Paint</h5>
        </div>
        <div>
          <h3>About</h3>
          <p>Journeys and Jazz: The Fruits of the Gods is a turn-based RPG created in RPG Maker MZ. 
            It features the four characters of Leonard, Seleth, Dreck, and Tezca as they explore the modern fantasy world of Eclysia for the titular Fruits of the Gods.
            The story will take place over 6 parts with parts 1 and 2 currently released and part 3 nearing completion.
            Play it for free on itch.io: (insert Link)
          </p>
          <h3>Process</h3>
          <p>Journeys and Jazz: The Fruit of the Gods (JNJ)'s story originated from my first ever Tabletop RPG campaign, using my original system, Journeys and Jazz.
            The game not only retells that story but features additional content that went unused in the campaign.
            I originally started this project as my Senior Thesis and currently am continuing to work on it in my spare time.
            One of my main focuses in this project is to have a game that can be comedic but also is not afraid to take itself seriously.
            Along with this, I value the expressiveness of the characters which is showcased through their many different portrait expressions.
          </p>
          <p>
            I find it very engaging to work on the combat system. 
            I work as hard as I can to make each skill a character gets interesting and to keep each playable character balanced with one another.
            One way I worked to give player's choice in combat is through equipment. 
            In JNJ, every item adjusts stats by a % rather then a flat value.
            This allowed me to keep items worthwhile throughout the game, including weapons.
            Each weapon is designed to fit a slightly different playstyle, making them sidegrades rather than upgrades.
            An example of this can be seen with three of Dreck's weapons. 
            The Cactus grants Dreck a higher attack boost than his other choices but he takes damage each turn.
            The Limbo Pole instead sacrifices attack in exchange for allowing Dreck to act more often.
            The standard Log instead is more balanced, boosting his defense and attack, making it the best general pick.
          </p>
          <h3>Challenges</h3>
          <p>
            While RPG Maker MZ makes the creation progress much easier with its premade assets, engine, and combat systems, this has the downside of being less customizable.
            I have occassionally struggled to implement my ideas due to it's restrictions though I have been able to still succeed whether it be by finding plugins that add functionality
            or editing the engine's code myself.
            I have also numerous times during my work on JNJ, faced creative burn out.
            This was especially difficult to pull through in Part 3 which features many more NPCs than Part 1 and 2 combined.
            I found switching my focus to other aspects or different projects helped greatly with giving me time to create more NPC ideas.
          </p>
          </div>
      </div>

      <div class="container">
        <div class="row">        
          <div class="Leo col">
            <div class="row ">
              <div class="col ">
              <img src="../assets/JNJ/Leonard.png" width="100%">
            </div>
            <div class="col ">
              <h2>Leonard</h2>
              <h3>The Great and Most Talented</h3>
              <p>Leonard is from the Eastern Archipelago. 
                He is a bard who feels he struggles to get the recognition he desires. 
                He hopes to join a grand adventure to write songs about that will top the charts.</p>
              <p>
                Leonard fills a supportive role; buffing and healing the party along with debuffing enemies. 
                He can also use Play Wildly, randomly damaging allies and foes alike in exchange for MP.
              </p>
            </div>  
            </div>
          </div>
          <div class="Sel col">
            <div class="row ">
              <div class="col ">
              <img src="../assets/JNJ/Seleth.png" width="100%">
            </div>
            <div class="col ">
              <h2>Seleth</h2>
              <h3>Princess of Malachite</h3>
              <p>Seleth was born in the northern continent of Malachite, known for its frost and magic.
                One day she ran away from home and is now searching for power to stop her mother.
              </p>
              <p>
                Seleth serves as the party’s tank and magic user excelling in taking hits and bypassing the high defense of some foes. 
                When her basic Ice spell isn’t enough, she can use Icicle Smash for heavy damage… if it hits.
              </p>
            </div>  
            </div>
          </div>
        </div>
        <div class="row">
          <div class="Dreck col">
            <div class="row ">
              <div class="col ">
              <img src="../assets/JNJ/Dreck.png" width="100%">
            </div>
            <div class="col ">
              <h2>Dreck</h2>
              <h3>Ogre from Another World</h3>
              <p>Not much about Dreck’s past is known but he doesn’t seem to be from Eclysia. 
                He also doesn’t seem to be here for any reason other than having fun.
              </p>
              <p>
                Dreck is a fighter, he can both take a hit and dish them out. With proper support, Dreck can crush his foes with his Strong Attack skill or weaken groups with Wide Swing.
              </p>
            </div>  
            </div>
          </div>
          <div class="Tez col">
            <div class="row ">
              <div class="col ">
              <img src="../assets/JNJ/Tezca.png" width="100%">
            </div>
            <div class="col ">
              <h2>Tezca</h2>
              <h3>Mysterious Shapeshifter</h3>
              <p>Tezca does not like to open up but it's clear this isn’t his first adventure. He belongs to an ancient race known as the Yunpek.
              </p>
              <p>
                Tezca is the party’s rogue. He is fast but isn’t able to take too many hits. He can handle most enemies with either his Dual Attack or his Armor Piercer. He can even use his enemies’ attack against them with Inverse Strike.
              </p>
            </div>  
            </div>
          </div>
        </div>

      </div>
      
  </template>
  <script>
  export default 
  {
      mounted () 
      {
        window.scrollTo(0, 0)
      }
  }
  </script>
  <style>
.Leo
{
  background-color:rgb(255, 147, 147);
  width:75%;

}
.Sel
{
  background-color:#cdebff;
  width:75%;
}
.Dreck
{
  background-color:rgb(204, 255, 181);
  width:75%;
}
.Tez
{
  background-color: rgb(170, 255, 227);
  width:75%;
}  

  </style>