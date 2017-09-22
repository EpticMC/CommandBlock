# CommandBlock

<p align="center">
<img height="300" width="auto" src="https://epticmc.com/images/cmd.png" />
</p>

<p align="center"> Collection of <a href="https://epticmc.com">EpticMC</a>'s CommandBlock commands, tools and scripts </p>

Everything from small commands like EntityData manipulations to bigger routine driven programs. <br>
Also check out [Commander IDE](https://github.com/EpticMC/Commander-IDE), a fully featured IDE/Editor for CommandBlock scripts!

### Contributing

If you'd like to add a a useful command or information to the list, please [create an issue](https://github.com/EpticMC/CommandBlock/issues) or fork this repository and submit a [pull request](https://github.com/EpticMC/CommandBlock/pulls). :blush:

**If you choose to make a Pull Request:** <br>
Please make yourself comfortable with Markdown Syntax first: [MarkDown Help](https://help.github.com/articles/github-flavored-markdown), [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) <br>
Also please try to stick to our style / layout so this markdown file stays consistent :smile: 


## Table of Contents:

- [EntityData Manipulation](#entitydata-manipulation)
  - [ArmorStands](#armorstands)
    - [Laying Item](#layingitem)
    - [Sitting Armorstand]()
    - [Guard]()
  - [NPC](#npc)
    - [Invulnerable Baby Chicken](#invchicken)
  - [Other Entities](other-entities)
    - [Invulnerable Ender Crystal](#crystal)
    - [De-Spawn Near Crystal](#despawncrystal)
- [...]()

-------

## EntityData Manipulation

### ArmorStands

\- Please give us some time to write the code -

<hr>

- <a name="layingitem"></a>Laying Item: <br><br>
Description: <br>
Spawn an invisible armorstand holding an item. Makes it look like its laying on the floor. <br><br>
CommandBlock Command: <br>
```Assembly
summon ArmorStand ~.5 ~-.8 ~-1 {DisabledSlots:1,NoGravity:true,Invisible:1,Invulnerable:0,Small:false,Equipment:[{id:0050,Count:1},{},{},{},{}],Pose:{RightArm:[0.0f,30.0f,0.0f]},Rotation:[30.10f,]}
```

<hr>

### NPC

- <a name="invchicken"></a>Invulnerable Baby Chicken: <br><br>
Description: <br>
Spawn AI Less Baby Chicken as invulnerable Entity <br><br>
CommandBlock Command: <br>
```Assembly
/summon Chicken ~1 ~.2 ~0 {Rotation:[55f],Invulnerable:1,NoAI:1,Silent:1,IsBaby:1,Age:-1000000000}
```

<hr>

### Other Entities

- <a name="crystal"></a>Invulnerable Ender Crystal: <br><br>
Description: <br>
Spawn invulnerable EnderCrystal with basis hidden in the ground <br><br>
CommandBlock Command: <br>
```Assembly
/summon EnderCrystal ~-1 ~-.1 ~ {Invulnerable:1}
```

<hr>

- <a name="despawncrystal"></a>Despawn near Ender Crystals: <br><br>
Description: <br>
Removes all Ender Crystals made invulnerable by the above command in a range of `1` block<br><br>
CommandBlock Command: <br>
```Assembly
/killall endercrystal 1
```

<hr>
