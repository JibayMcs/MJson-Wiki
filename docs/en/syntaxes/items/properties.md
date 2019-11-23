# `properties` object

!!! info  
    👷 🚧 This Page is currently under construction ! 🏗️ 👷‍♀️
    

You can define properties to deep customize your item.  
??? info "It equals to the Java code"
    ```java
    new ItemWithProperties(new Item.Properties().([...]));
    ```

??? note "Example"

    ```json
    [
      {
        "registryName": "test_with_properties",
        "properties": {
          "toolType": "pickaxe",
          "toolTypeLevel": 1,
          "containerItem": "minecraft:bucket",
          "maxDurability": "20",
          "food": "APPLE",
          "maxStackSize": "64",
          "noRepair": false,
          "rarity": "COMMON"
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
              "toolType": "pickaxe",
              "toolTypeLevel": 1,
              "containerItem": "minecraft:bucket",
              "maxDurability": "20",
              "food": "APPLE",
              "maxStackSize": "64",
              "noRepair": false,
              "rarity": "COMMON"
            }
          },
          {
            "registryName": "test_with_other_properties",
            "properties": {
              "maxStackSize": "1",
              "noRepair": true
            }
          }
        ]
        ```

## Values