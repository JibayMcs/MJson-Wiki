# The `items.json` structure

!!! info  
    👷 🚧 This Page is currently under construction ! 🏗️ 👷‍♀️
    
!!! info "Prerequisites"
    To understand whats following, ensure to have read the [Content Pack Files Structure](../content_pack.md) page.
    

`objects/items.json` was designed to register all the new items you want for Minecraft  

That's a **JsonArray** file, it always start with `[]`

___

## Create a Simple Item

A simple item can be registered only with the <sup>**(mandatory)**</sup> `registryName` object.

??? note "Example"

    ```json
    [
      {
        "registryName" : "my_supa_item"
      }
    ]
    ```

    ??? note "Example with multiple items"
    
        ```json
        [
           {
             "registryName" : "my_supa_item"
           },
           {
              "registryName" : "my_supa_other_item"
           },
           {
              "registryName" : "yeah_iteeeeeeems"
           }            
        ]
        ```

___

### Create a Complex Item

You can customize your item with some <sub>**(optional)**</sub> json objects.

- `"properties"` [How To](items/properties.md)
- `"itemGroup"` [How To](items/itemGroup.md)

!!! warning
    If these objects are **empty**, **null** or **misspelled**, they are <u>ignored</u>.
    
___