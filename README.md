# CommandBlock

<p align="center">
<img height="300" width="auto" src="https://pre00.deviantart.net/7a6f/th/pre/f/2016/209/0/1/commandblock_animationtest10038_by_iggykoopa321-dabr12y.png" />
</p>

<p align="center"> Collection of <a href="https://epticmc.com">EpticMC</a>'s CommandBlock commands, tools and scripts </p>

Everything from small commands like EntityData manipulations to bigger routine driven programs. <br>
Also check out [Commander IDE](https://github.com/EpticMC/Commander-IDE) by EpticMC, a fully featured IDE/Editor for CommandBlock scripts!

Check out this awesome tool for positioning armorstands as well: <br>
http://haselkern.com/Minecraft-ArmorStand/

**Note:** All commands have _only_ been tested on version **1.8**

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
    - [Giant Sword](#giantsword)
  - [Other Entities](other-entities)
    - [Invulnerable Ender Crystal](#crystal)
    - [De-Spawn Near Crystal](#despawncrystal)
    - [Chest with item](#chestitem)
- [Contributors](#contributors-heart)
- [...]()

-------

## EntityData Manipulation

### ArmorStands

\- Please give us some time to write the code -

<hr>

- <a name="layingitem"></a>Laying Item: <br><br>
Description: <br>
Spawn an invisible armorstand holding an item (torch in this case). Makes it look like its laying on the floor. <br><br>
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

- <a name="giantsword"></a>Giant Sword: <br><br>
Description: <br>
Spawn AI Less, Invisible Giant holding a sword. Looks like a huge floating sword. <br><br>
CommandBlock Command: <br>
```Assembly
/summon Giant ~ ~ ~ {Equipment:[{id:diamond_sword},{},{},{},{}],Attributes:[{Name:generic.followRange,Base:0},{Name:generic.knockbackResistance,Base:1}],ActiveEffects:[{Id:14,Amplifier:1,Duration:999999,Ambient:1}],NoAI:1,Silent:1}
```

<hr>

### Guards for HubServer:

Block Placement:

<img src="https://raw.githubusercontent.com/EpticMC/CommandBlock/master/2019-08-09_04.22.11.png" widh="100%" height="auto">

**North-West** 

Guard:
```Assembly
/summon ArmorStand ~0 ~.85 ~-1 {Invulnerable:1b,PersistenceRequired:1b,NoBasePlate:1b,NoGravity:1b,ShowArms:1b,Rotation:[312f],Pose:{Head:[14f,0f,0f],LeftLeg:[12f,0f,357f],RightLeg:[355f,0f,3f],LeftArm:[284f,32f,0f],RightArm:[286f,327f,0f]}}
```

Sword:
```Assembly
/summon ArmorStand ~-.66 ~.7 ~.55 {NoGravity:1b,ShowArms:1b,Invisible:1b,Rotation:[320f],Pose:{RightArm:[170f,89f,90f]}}
```

**North-East** 

Guard:
```Assembly
/summon ArmorStand ~1.14 ~.85 ~-.14 {Invulnerable:1b,PersistenceRequired:1b,NoBasePlate:1b,NoGravity:1b,ShowArms:1b,Rotation:[45f],Pose:{Head:[14f,0f,0f],LeftLeg:[12f,0f,357f],RightLeg:[355f,0f,3f],LeftArm:[284f,32f,0f],RightArm:[286f,327f,0f]}}
```

Sword:
```Assembly
/summon ArmorStand ~-.45 ~.7 ~-.9 {NoGravity:1b,ShowArms:1b,Invisible:1b,Rotation:[45f],Pose:{RightArm:[170f,89f,90f]}}
```

**South-East** 

Guard:
```Assembly
/summon ArmorStand ~.02 ~.85 ~1.1 {Invulnerable:1b,PersistenceRequired:1b,NoBasePlate:1b,NoGravity:1b,ShowArms:1b,Rotation:[145f],Pose:{Head:[14f,0f,0f],LeftLeg:[12f,0f,357f],RightLeg:[355f,0f,3f],LeftArm:[284f,32f,0f],RightArm:[286f,327f,0f]}}
```

Sword:
```Assembly
/summon ArmorStand ~.8 ~.7 ~-.5 {NoGravity:1b,ShowArms:1b,Invisible:1b,Rotation:[145f],Pose:{RightArm:[170f,89f,90f]}}
```

**South-West** 

Guard:
```Assembly
/summon ArmorStand ~-1.05 ~.95 ~.11 {Invulnerable:1b,PersistenceRequired:1b,NoBasePlate:1b,NoGravity:1b,ShowArms:1b,Rotation:[225f],Pose:{Head:[14f,0f,0f],LeftLeg:[12f,0f,357f],RightLeg:[355f,0f,3f],LeftArm:[284f,32f,0f],RightArm:[286f,327f,0f]}}
```

Sword:
```Assembly
/summon ArmorStand ~.5 ~.7 ~.8 {NoGravity:1b,ShowArms:1b,Invisible:1b,Rotation:[225f],Pose:{RightArm:[170f,89f,90f]}}
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

- <a name="chestitem"></a>Chest with item: <br><br>
Description: <br>
Spawns a chest with an item (sword in this case) in it<br><br>
CommandBlock Command: <br>
```Assembly
/summon FallingSand ~ ~1 ~ {TileID:54,Time:1,TileEntityData:{Items:[{id:276,tag:{display:{Name:"Black Sword"}}}]}}
```

<hr>

## Contributors :heart:

- [**@NLDev**](https://github.com/NLDev)
- [**@Fr3shlama**](https://github.com/Fr3shlama)
