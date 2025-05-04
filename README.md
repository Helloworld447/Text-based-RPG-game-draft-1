# Text-based-RPG-game-draft-1


**Name of the project**: Paladin's Quest: Obsidian Oath

**Member names and GitHub handles**: 
  Nidu Rahubedde(https://github.com/Helloworld447)
  Russell Villanueva (https://github.com/RussellVillanueva)
  Diego Delgado (
  Elizabeth Gonzalez Ruiz (https://github.com/Elizabeth-rruiz)

**Wny is it interesting to us?**
A majority of our members have played video games as kids, especially the nostalgic rpg-styled games. So, the chance to create our own game from scratch is quite exhilarating. 

**What languages/tools/technologies do you plan to use?**
We plan on using Python --we have already confirmed our selection with Professor Reem Ali. In addition to that, we're also deciding on which libraries to use. This may change as we proceed because upcoming functions will need various dependencies. But we will adequately document the process :)

**What will be the input/output of your project?**

Inputs:
.Player commands: 1,2,3 to select dice outcomes. Keywords to tell system what to do (roll, stats, use potion, quit, etc)

.Use random to trigger rolls

Outputs:
.Narration from dungeon-master styled text blocks 

.Combat and event results

.Player's stat display (health, inventory, etc)

.Story progression updates!

**What are the features that the project provides?**

The idea is that the user plays a Paladin, a sworn protector of a small town called Amberwater. A corrupt sorcerer seeks to conquer the obsidian-rich hometown so that he can open a portal to the Nether. He does this so that he can return home; however, doing so will release unspeakable evil in Amberwater. So, our user must go through 7 levels, each with it's own quest,options, puzzles, and even monsters. Here's a rough idea of what we're thinking of implementing:

.Each level has unique story elements tied to the sorcerer's plans. And each level also introduces puzzles, monsters, and environmental challenges (maybe hail affecting specfic abilities, etc)

.Use of a 3-sided die: 
      Combat(attack, defend, special ability)
      Exploration(left, right, Secret)
      Puzzle outcomes(correct, partial, fail)

.Paladin has health, strength stats

.Inventory and loot system: Potions, keys(open doors/chests), maybe even scrolls granting special abilities. Maybe even some items offer moral trade-offs (ex: power at a cost)

.Each decision that the user makes will lead to branching paths and even multiple endings.

.Final battle with the sorcerer at level 7. Boss will have more health and the choices for the user will also be harder.

**Description of Class diagram**

Game: Manages the overall flow. Controls which level the player is currently in, story progression, and checks user input. Handles loading enemies and calling player/enemy actions.

Level : Represents one stage in the game. Each level has its own unique story (tied to the sorcerer's plan), a puzzle to solve, enemies to fight and environmental effects. The start_level() method sets the stage. The trigger_event () method randomly introduces environmental effects of special challenges. 

Puzzle : A helper class used within each level. Contains logic to present the puzzle and check the player’s response. Puzzle outcomes (correct, partial, fail) are determined using a three-sided die.

Player: Represents the main character, the Paladin. Stores the player’s stats (health, strength) and inventory. Methods allow for attacking, exploring, using items, and displaying stats. Combat outcomes (attack, defend, special) and exploration choices (left, right, secret) are influenced by a three-sided die. Choices made by the player impact story direction.

Item: Represents collectable or usable objects like potions, keys, scrolls, or loot. Some items may restore health or unlock doors, while others grant abilities or offer power at a cost. Stored in the player’s inventory.

Enemy : Represents enemies that the player fights during each level. Each enemy has its own health and attack power. Methods include attacking the player and checking if it is still alive. 

Final Boss : Inherited from the Enemy class. This is a special type of enemy with additional abilities like … (to be discussed) Only appears in level 7. 

ThreeSidedDie: Simulates randomness for game decisions. Used to determine outcomes in combat (attack, defend, special), exploration (left, right, secret), and puzzle-solving (correct, partial, fail). 