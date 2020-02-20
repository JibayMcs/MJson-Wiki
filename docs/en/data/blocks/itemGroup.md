# `itemGroup` object

To put your fresh new block in a Creative Tab, you can define an `itemGroup`

By default if this parameter is not defined, your block is in the Misc/Material Creative Tab.

!!! tip "[Create your own creative tab](../../itemgroup/)"
    

!!! note "Example with vanilla creative tab"  
    
    ```json
    [
      {
        "registryName": "my_supa_block",
        "itemGroup" : "minecraft:redstone"
      }
    ]
    ```
    
___

!!! note "Example with custom creative tab"  
    
    ```json
    [
      {
        "registryName": "my_supa_block",
        "itemGroup" : "super_pack:my_tab"
      }
    ]
    ```