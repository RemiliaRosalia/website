<template>
<div class="projectPage">
    <!-- <h1>Gift of Pain</h1> -->
    <h1>Save The Princess</h1>
    <div class="projectIMG">
      <h5>Tools used: RPG Maker MZ, JavaScript, Clip Studio Paint</h5>
    </div>
    <div>
      <p>
        Save the Princess is a small RPG game I created for my partner and while there is no playable version, this page will describe the game.
        I used this project as a way to experiment more with turn based mechanics and RPG Maker as a whole in ways that I am unable to do with <a target="_blank" href="https://remiliarosalia.itch.io/jnj-fruits-of-the-gods">Journeys and Jazz: The Fruits of the Gods.</a>
        One of these changes was a more standard turn base system rather than the Time Progress version used in Journeys and Jazz.
      </p>
      <h2>Classes</h2>
      <p>
        One of the main aspects I wanted to experiement with was balancing around only a single character who can change classes.
        Save the Princess features 6 classes, 2 of which being rarer.
        The classes are:
      </p>
        <p>● Knight, a physically defensive class with good attack</p>
        <p>● Mage, a physically frail class that can deal heavy magic damage</p>
        <p>● Cleric, a defensive magic class with all around even stats</p>
        <p>● Rogue, a quick class that has strong debuffs but low defenses</p>
        <p>● God Slayer, a powerful class based on the God Slayer from Journeys and Jazz</p>
        <p>● Malachite Mage, a defesive class based on Seleth from Journeys and Jazz</p>
      <p>  
        Each class has their own strengths and weaknesses and the player is able to switch between them by using special items that either switch to a specific class or a random one.
      </p>
      <h2>Loot System</h2>
      <p>
        Rather than gaining an enemy's items after combat, they instead give 'loot' items that when used, give a random item from a selection based on the enemy it belongs to, not unlike a gacha game system.
        These items range from armors and weapons to small permanent stat increases. I decided to try this out as not only does my partner like gacha systems, it also meant I was not limited to RPG Makers 3 possible drops per enemy limitation.
      </p>
      <h2>Weapon Buffs</h2>
      <p>
        With the player being able to change classes easily, I wanted weapons to be stronger for certain classes without outright limiting them to only one class.
        I accomplished this by taking inspiration from Dokapon Kingdom where weapons give a percentage boost when used by matching classes.
        In Save the Princess each class has a designated weapon type and when the player is using the matching class, they are given an additional 15% boost to their attack and magic attack stats.
      </p>
      <h2>Other Gear</h2>
      <p>
        Another difference between Save the Princess and Journeys and Jazz is that instead of having 3 accessory slots for any item, the player has 4 slots; helmet, chest, shield, and accessory.
        Also unlike Journeys and Jazz, these items give flat boosts to stats instead of percentages.
        I made these changes as a way to experiment with a less free form gear system.
      </p>
      <h2>Forest Map</h2>
      <p>
        This is the first area the player visits ignoring a small starting town. It serves as a simple dungeon with paths interconnecting and splitting off often. This area does not use random encounters and instead has enemies wander around and chase the player if they get too close.
        There are also plenty of spots where the player can find items on the ground.
        When the player reaches the end, they find a campfire to heal at and if they continue, they face the first boss.
      </p>
      <h2>The Four Trials</h2>
      <p>
        After defeating the boss, the player arrives at the Dark Lord's Castle and must pass 4 trials, each based on one of the four main classes and can be fought in any order.
        While standard enemies do not scale, the boss of each trial does get stronger based on how many trials have been completed.
        
      </p>
      <h4>The Knight Trail</h4>
      <p>The knight trial involves the player going through four fights each with a randomized gimmick such as enemies having a higher critical rate, the player being unable to use MP, both sides being poisoned, and more. 
        The player cannot use items in the battles but can in between but if they leave the area, they have to start from the beginning.
        Once all four fights have been won, the player then fights against the boss and passes the trial.
      </p>

      <h4>The Mage Trail</h4>
      <p>
        This trial is a puzzle where the player watches an npc travel along an invisible path and must follow it. If the player makes a mistake, they fall, being forced into a fight, and then has to start from the beginning.
        In order to make this trial forgiving, the correct tiles change so the player does not need to worry about remembering the earlier parts each time.
        There are also floating fires to help in memorizing when to turn.
        Once the player completes both rooms, they then can face the boss.
      </p>
      
      <h4>The Cleric Trail</h4>
      <p>
        This trial is inspired by the Game Boy Advance version of Final Fantasy I's bonus dungeons.
        In the trial there are npcs scattered around and the player must complete a fetch quest, talking to npcs in the right order based on hints.
        If the player bumps into a wrong npc, they are forced into a battle and the npc disappears.
        Once the player talks to 5 npcs in the right order, they are able to battle the boss of the area.
      </p>
      
      <h4>The Rogue Trail</h4>
      <p>
        This trial focuses on dodging traps. The first room has fire balls being launched in a corridor and the player must duck in and out of cover to reach the end.
        The second room has some bolders going around the perimeter and the player must fit in between to get to the opening at the end. The final room again has the player dodging flames though in a different pattern.
        If the player at any point gets hit by an obstacle, they are forced into a battle.
        Once all three rooms have been navigated successfully, the player is able to battle the boss.
      </p>
      <p>
        After completting the four trials, the player can access two optional bosses at the areas entrance along with being able to continue to the final trial.
      </p>
      <h4>The Final Trail</h4>
      <p>
        I decided that a fun final trial for my partner would be for them to have to go through a trivia show about me.
        The trivia show was a challenge to create with me having to really learn how to utilze RPG Maker MZ's scripting as it does not allow for text variables otherwise, let alone the 3D array I needed for it to work.
        This trial has fights whenever the player answers incorrectly and the enemies are a mix of those from the other trial.
        Once the player finishes this trial, they are free to fight the final boss of the game.
      </p>
      <h2>Enemies</h2>
      <p>
       I followed a similar design phillosophy as Journeys and Jazz: The Fruits of the Gods with enemies in this project.
       Whenever the player first enters an area, encounters can be relatively difficult but as the player levels up and gains items, the fights become much easier.
       This difficulty curve ends with a decently strong boss then starts all over again for the next area.

       I also decided to play more with enemies being weak to elements which is enhanced by every class having its own selection
       of elements. This added strategy such as using Mage when enemies were weak to fire or Cleric if they are weak to light.
      
      The next part of this section will focus on a few specific enemies I find especially interesting.
      </p>
      <h4>Imp</h4>
      <p>
        This enemy is most similar to one of my original ideations for this project where enemies could lower your stats or even change your class mid combat.
        These ideas were shelved and the closest similarity is that the Imp is able to steal some of the player's exp which can even delevel them. If the player is then defeated, they do not gain the exp back.
        Besides that, the Imp has some magic attacks and can debuff the player's attack and magic attack.
      </p>
      <h4>Demon Count</h4>
      <p>
        The boss of the Mage Trial. The count, similar to the Mage class, has powerful magic attacks.
        Unlike the Mage class, he can also summon slightly weaker Imps (which lack the EXP steal skill) to aid him.
        Being a magic focused enemy, he is weak to the Cleric's Silence skill.
      </p>
      <h4>Death</h4>
      <p>
        The boss of the Rogue Trial. Death is strong and fast but does not have much defense.
        The signiture skill of this fight is called Heartless Angel, named after the move of the same name Sephiroth uses in the Kingdom Hearts' games.
        This skill takes 2 turns and if the player does not deal damage before the second part, they are reduced to 1 HP.
        With Deaths high speed stat, it can be difficult for an unsuspecting player avoid it.
      </p>
      <h4>God Slayer and Malachite Queen</h4>
      <p>
        The 2 optional bosses, both are directly based on the rare classes and share the same skills with those classes. God Slayer is realatively similar to the God Slayer boss fight in Journeys and Jazz: The Fruits of the Gods.
        These fights were originally decided so that the God Slayer and Malachite Mage class would be able to gain their final their of weapons as the bosses of the four trials can drop the final tier for their respective class.
      </p>

      
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
  h2
  {
    text-align: center;

  }
  h4
  {
    text-align: center;
    /* margin-right: 30%; */
  }
</style>
  