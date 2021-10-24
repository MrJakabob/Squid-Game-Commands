# Squid-Game-Commands
Here's the commands used in my video
---------------Armor Stands-----------------
/summon armor_stand ~ ~ ~ {CustomName:"\"Forward\"",invisible:1,NoGravity:1}
/summon armor_stand ~ ~ ~ {CustomName:"\"Backward\"",invisible:1,NoGravity:1}

-------------------Timer--------------------
/scoreboard objectives add Timer dummy
/scoreboard players set 1s Timer 20

-------------------Chain--------------------
/scoreboard players add timer4s Timer 1
/execute if score timer4s Timer >= 4s Timer
/scoreboard players set timer4s Timer 0
setblock x y z minecraft:redstone_block

-------------------Check--------------------
/execute at @a run tp @e[type=minecraft:armor_stand,name=Forward] ~2 ~ ~
/execute at @a run tp @e[type=minecraft:armor_stand,name=Backward] ~-2 ~ ~
/setblock x y z minecraft:gold_block
/execute at @e[type=minecraft:armor_stand,name=L] run execute if entity @a[distance=..1.99] run setblock x2 y2 z2 green_wool
/execute at @e[type=minecraft:armor_stand,name=R] run execute if entity @a[distance=..1] run setblock x2 y2 z2 minecraft:redstone_block


