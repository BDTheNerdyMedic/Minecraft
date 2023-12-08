# Common Server Commands

## Performance monitoring

### Query

#### Report a count of each item drop within the overworld
    /execute in minecraft:overworld run execute as @e[type=item] run data get entity @s Item.Count

### Observable

#### Run Observable for 30 seconds
    observable run 30

## Server Recovery

### Kill Command

#### Remove all item drops from the overworld
    /kill @e[type=item]

#### Remove all item drops within 100 blocks from a specific location
    /kill @e[type=item,x=0,y=0,z=0,distance=..100]

### Setblock Command

#### Replace a block with air without dropping the block or it's inventory
    /setblock 0 0 0 air replace

[< Back](index.md)
