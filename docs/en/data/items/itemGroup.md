# `itemGroup` object

To put your fresh new item in a Creative Tab, you can define an `itemGroup`

By default if this parameter is not defined, your item is in the Misc/Material Creative Tab.

!!! tip "[Create your own creative tab](../../itemgroup/)"
    

!!! note "Example with vanilla creative tab"  
    
    ```json
    [
      {
        "registryName": "my_supa_item",
        "itemGroup" : "minecraft:redstone"
      }
    ]
    ```
    
___

!!! note "Example with custom creative tab"  
    
    ```json
    [
      {
        "registryName": "my_supa_item",
        "itemGroup" : "super_pack:my_tab"
      }
    ]
    ```