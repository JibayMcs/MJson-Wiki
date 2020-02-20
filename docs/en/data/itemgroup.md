# The `itemgroup.json` structure

!!! info "Prerequisites"
    To understand whats following, ensure to have read the [Content Pack Files Structure](../content_pack.md) page.

All fresh new json are **JsonObject** file, there always starts with `{}`
___

### Create your Creative Tab

!!! note "Example"
    
    ```json
    {
      "registryName": "my_tab", //mandatory
      "itemIcon": "minecraft:dirt", //mandatory
      "noTitle": false, //optional
      "hasSearchBar": true, //optional
      "hasScrollBar": false, //optional
      "backgroundImage" : "my_background.png" //optional
    }
    ```
    
## Values

??? abstract "`registryName`"
    Refer to an **unique registry name** for your item group<br>
    For uses in **Blocks** or **Items**, call it with your declared `namespace` in [content.pack](../content_pack.md#contentpack)<br>
    Example: `my_super_pack:my_tab`
??? abstract "`itemIcon`"
    Use registry name of items or block to create an icon of your Creative Tab  
    `minecraft:dirt` or `super_pack:my_block` for example  
    
    !!! tip "[Check blocks list on Minecraft Wiki](https://minecraft.gamepedia.com/Block)"
    
??? abstract "`noTitle` **(boolean)**"
    Show Creative Tab title ?  
    `default: true`
    
??? abstract "`hasSearchBar` **(boolean)**"
    Has a search bar on top of the Creative Tab ?  
    `default: false`
    
??? abstract "`hasScrollBar` **(boolean)**"
    Has a scroll bar to the right of the Creative Tab ?  
    `default: false`

??? abstract "`backgroundImage`"
    
    !!! warning   
    
        The background texture need to go in:  
        `assets/content_pack_id/textures/gui/container/creative_inventory/`  
        And the texture file need to start with `tab_`
        
    !!! note "Example"
           
        `assets/super_pack/textures/gui/container/creative_inventory/tab_my_background.png`
        

___

### Vanilla Creative Tabs

??? example "List of Vanilla Creative Tabs"
    `minecraft:blocks`  
    `minecraft:decoration`  
    `minecraft:redstone`  
    `minecraft:transportation`  
    `minecraft:food`  
    `minecraft:tools`  
    `minecraft:combat`  
    `minecraft:brewing`  
    `minecraft:misc`  