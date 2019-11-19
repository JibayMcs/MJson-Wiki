# `properties` object

You can define properties to deep customize your block.  
??? info "It equals to the Java code"
    ```java
    new BlockTestWithProperties(Block.Properties.create([...]));
    ```

??? note "Example"

    ```json
    [
      {
        "registryName": "test_with_properties",
        "properties": {
          "material": "WOOL",
          "hardness": 1,
          "resistance": 1,
          "lightValue": 0,
          "soundType": "SAND",
          "harvestLevel": 1,
          "harvestTool": "axe",
          "slipperiness": 1,
          "hasVariableOpacity": false,
          "noDrops": false,
          "doesNotBlockMovement": false
        }
      }
    ]
    ```
    
    ??? note "Example with multiple blocks"
    
        ```json
        [
          {
            "registryName": "test_with_properties",
            "properties": {
              "material": "WOOL",
              "hardness": 1,
              "resistance": 1,
              "lightValue": 0,
              "soundType": "SAND",
              "harvestLevel": 1,
              "harvestTool": "axe",
              "slipperiness": 1,
              "hasVariableOpacity": false,
              "noDrops": false,
              "doesNotBlockMovement": false
            }
          },
          {
            "registryName": "test_with_other_properties",
            "properties": {
              "material": "CLAY",
              "lightValue": 16,
              "soundType": "GLASS"
            }
          }
        ]
        ```

## Values

??? abstract "`material`"  
    Define a "physics" of a blocks.  
    With `ROCK` material can only be destroyed by pickaxe, unlike `GROUND` materials, and those with `WOOD` material can burn.  
    
    ??? snippet "List of all existing Materials"  
        **AIR  
        STRUCTURE_VOID  
        PORTAL  
        CARPET  
        PLANTS  
        OCEAN_PLANT  
        TALL_PLANTS  
        SEA_GRASS  
        WATER  
        BUBBLE_COLUMN  
        LAVA  
        SNOW  
        FIRE  
        MISCELLANEOUS  
        WEB  
        REDSTONE_LIGHT  
        CLAY  
        EARTH  
        ORGANIC  
        PACKED_ICE  
        SAND  
        SPONGE  
        SHULKER  
        WOOD  
        BAMBOO_SAPLING  
        BAMBOO  
        WOOL  
        TNT  
        LEAVES  
        GLASS  
        ICE  
        CACTUS  
        ROCK  
        IRON  
        SNOW_BLOCK  
        ANVIL  
        BARRIER  
        PISTON  
        CORAL  
        GOURD  
        DRAGON_EGG  
        CAKE**  

??? abstract "`hardness` **(decimal)**"
    "Hardness" to breaking with a pickaxe or shovel, depending on the `material`  

??? abstract "`resistance` **(decimal)**"
    Explosions resistance

??? abstract "`lightValue` **(integer)**"
    Intensity of light produced by the block  
    **Max Value: 16**  

??? abstract "`soundType`"  
    The sound of the block on walking on, breaking, etc.  
    
    ??? snippet "List of all existing Sounds Types"  
        **WOOD  
        GROUND  
        PLANT  
        STONE  
        METAL  
        GLASS  
        CLOTH  
        SAND  
        SNOW  
        LADDER  
        ANVIL  
        SLIME 
        WET_GRASS  
        CORAL  
        BAMBOO  
        BAMBOO_SAPLING  
        SCAFFOLDING  
        SWEET_BERRY_BUSH  
        CROP  
        STEM  
        NETHER_WART  
        LANTERN**    

??? abstract "`harvestLevel` **(integer)**"  
    This value assigns what tier of Harvest level is required to mine it.
        
    !!! info "Harvest Level"  

        **0** Gold/Wood  
        **1** Stone  
        **2** Iron  
        **3** Diamond        
    
??? abstract "`harvestTool`"
    What item can break it. `axe`, `pickaxe` or `shovel` ?

??? abstract "`slipperiness` **(decimal)**"  
    Like the **Ice Block**, is it a slippery block ?

??? abstract "`hasVariableOpacity` **(boolean)**"  
    That's a transparent block like Glass ?
    
??? abstract "`noDrops` **(boolean)**"  
    This block can be dropped himself ?
    
??? abstract "`doesNotBlockMovements` **(boolean)**"  
    If ``true`` this block is traversable.  
    Like Sapplings, Web, etc.