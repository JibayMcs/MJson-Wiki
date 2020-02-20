!!! info  
    👷 🚧 This Page is currently under construction ! 🏗️ 👷‍♀️
    

# A `biome.json` structure

!!! info "Prerequisites"
    To understand whats following, ensure to have read the [Content Pack Files Structure](../content_pack.md) page.

The folder `objects/biomes/` was designed to register all the new biomes you want for Minecraft  

All fresh new json are **JsonObject** file, there always starts with `{}`

___

# Understanding the json structure

!!! danger "Some Precisions"
    Creating biome are the most complicated thing.<br>
    It take so many parameters and the possibilities are so great,<br>
    That it's easy to get lost...<br>
    And you're probably going to take a long time before you get to a correct result.
    <br>
    Create biome at your own risk !

    !!! tip "Take a look at [Biomes examples](#biomes-examples)"

___

# Biomes examples



??? tip "Blueish forest type frozen biome"
    ??? note "`objects/biomes/test_biome.json`"
    
        ```json
        {
          "registryName": "test_biome",
          "category": "FOREST",
          "surface": {
            "surfaceBuilderType": "DEFAULT",
            "terrainConfig": {
              "topBlock": "minecraft:grass_block",
              "undergroundBlock": "minecraft:gravel",
              "underWaterBlock": "minecraft:sandstone"
            }
          },
          "climat": {
            "rainType": "SNOW",
            "temperature": 0.1,
            "downfall": 1
          },
          "biomeColor": {
            "waterColor": 4159204,
            "waterFogColor": 329011,
            "grassColor": 7512804,
            "foliageColor": 10400234
          },
          "biomeType": "WARM",
          "depth": 0.125,
          "scale": 0.05,
          "weight": 1000,
          "biomeDictionaryTypes": [
            "FOREST"
          ],
          "spawns": [
            {
              "entityClassification": "CREATURE",
              "entity": "minecraft:pig",
              "weight": 12,
              "minMaxGroupCount": 4
            }
          ],
          "carvers": [
            {
              "type": "AIR",
              "carver": "CAVE",
              "probability": 0.14285715
            },
            {
              "type": "AIR",
              "carver": "CANYON",
              "probability": 0.02
            }
          ],
          "structures": [
            {
              "name": "minecraft:mineshaft",
              "config": "MINESHAFT",
              "probability": 0.004,
              "mineshaftType": "NORMAL"
            },
            {
              "name": "minecraft:stronghold"
            },
            {
              "name": "minecraft:stronghold"
            },
            {
              "name": "minecraft:village",
              "config": "VILLAGE",
              "startPool": "minecraft:village/plains/town_centers",
              "size": 32
            }
          ],
          "features": [
            {
              "decoration": "TOP_LAYER_MODIFICATION",
              "feature": {
                "name": "freeze_top_layer"
              }
            },
            {
              "decoration": "VEGETAL_DECORATION",
              "feature": {
                "name": "minecraft:random_selector",
                "config": "MULTIPLE_RANDOM",
                "multipleRandomFeature": {
                  "features": [
                    {
                      "name": "birch_tree"
                    },
                    {
                      "name": "dark_oak_tree"
                    }
                  ],
                  "featureProperties": {
                    "name": "minecraft:normal_tree"
                  }
                },
                "probabilities": [
                  0.2,
                  0.1
                ]
              },
              "placement": {
                "name": "minecraft:count_extra_heightmap",
                "config": "COUNT_EXTRA_HEIGHTMAP",
                "count": 10,
                "extraChance": 0.1,
                "extraCount": 1
              }
            }
          ]
        }
        ```
    
    ??? info "In-game Render"
        ![Test Biome](../../../images/icy-forest-biome.png)

??? tip "Reddish desert type biome with monsters"
    ??? note "objects/biomes/biome_with_monsters.json"
    
        ```json
        {
          "registryName": "biome_with_monsters",
          "category": "DESERT",
          "surface": {
            "surfaceBuilderType": "DEFAULT",
            "terrainConfig": {
              "topBlock": "minecraft:red_sand",
              "undergroundBlock": "minecraft:red_sand",
              "underWaterBlock": "minecraft:bricks"
            }
          },
          "climat": {
            "rainType": "NONE",
            "temperature": 2,
            "downfall": 0
          },
          "biomeColor": {
            "waterColor": 4159204,
            "waterFogColor": 329011
          },
          "biomeType": "DESERT",
          "depth": 0.125,
          "scale": 0.05,
          "weight": 1000,
          "biomeDictionaryTypes": [
            "HOT",
            "DRY",
            "SANDY",
            "JUNGLE",
            "SWAMP"
          ],
          "spawns": [
            {
              "entityClassification": "MONSTER",
              "entity": "minecraft:spider",
              "weight": 100,
              "minMaxGroupCount": 4
            },
            {
              "entityClassification": "MONSTER",
              "entity": "minecraft:creeper",
              "weight": 100,
              "minMaxGroupCount": 4
            },
            {
              "entityClassification": "MONSTER",
              "entity": "minecraft:zombie",
              "weight": 100,
              "minMaxGroupCount": 4
            },
            {
              "entityClassification": "MONSTER",
              "entity": "minecraft:zombie_villager",
              "weight": 10,
              "minMaxGroupCount": 4
            },
            {
              "entityClassification": "MONSTER",
              "entity": "minecraft:husk",
              "weight": 100,
              "minMaxGroupCount": 4
            },
            {
              "entityClassification": "MONSTER",
              "entity": "minecraft:stray",
              "weight": 100,
              "minMaxGroupCount": 4
            },
            {
              "entityClassification": "MONSTER",
              "entity": "minecraft:silverfish",
              "weight": 10,
              "minGroupCount": 1,
              "maxGroupCount": 4
            }
          ]
        }
        ```
        
    ??? info "In-game Render"
        ![Red Desert Biome](../../../images/red-desert-biome.png)