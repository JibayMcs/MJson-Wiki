# A `block.json` structure

!!! info "Prerequisites"
    To understand whats following, ensure to have read the [Content Pack Files Structure](../content_pack.md) page.

The folder `objects/blocks/` was designed to register all the new blocks you want for Minecraft  

All fresh new json are **JsonObject** file, there always starts with `{}`

___

### Create a Simple Block

A simple block can be registered only with the <sup>**(mandatory)**</sup> `registryName` object.

??? note "Example"

    ```json
    [
      {
        "registryName" : "my_supa_block"
      }
    ]
    ```

    ??? note "Example with multiple blocks"
    
        ```json
        [
           {
             "registryName" : "my_supa_block"
           },
           {
              "registryName" : "my_supa_other_block"
           },
           {
              "registryName" : "yeah_bloooiiiiick"
           }            
        ]
        ```

___

### Create a Complex Block

You can customize your block with some <sub>**(optional)**</sub> json objects.

- `"properties"` [How To](blocks/properties.md)
- `"itemGroup"` [How To](blocks/itemGroup.md)
- `"voxelShape"` [How To](blocks/voxelShape.md)

!!! warning
    If these objects are **empty**, **null** or **misspelled**, they are <u>ignored</u>.
    
___
