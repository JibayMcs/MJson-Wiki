### The `blocks.json` syntax

!!! info "Prerequisites"
    To understand whats following, ensure to have read the [Content Pack Files Structure](../content_pack.md) page.

`objects/blocks.json` was designed to register all the new blocks you want for Minecraft  

That's a **JsonArray** file, it always start with `[]`

### Create a Simple Block

A simple block can be registered only with the `registryName` object.

??? bug "Example"

    ```json
    [
      {
        "registryName" : "my_supa_block"
      }
    ]
    ```

    ??? bug "Example with multiple blocks"
    
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