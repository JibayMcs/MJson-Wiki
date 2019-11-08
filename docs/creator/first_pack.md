




# Your first Content Pack

### Content Pack Files Structure
First at all, you need to understand the content pack files hierarchy.  

#### Zip File Structure
```
📁 Content Pack Root
├─	📝 content.pack
├─	📝 pack.mcmeta    
├─	🖼️ pack.png
│
├── 📁 assets
│   
└── 📁 objects
	├─	📝 blocks.json
    ├─	📝 items.json
	└─	📝 itemgroup.json
```

#### Content Pack zip file directory
-   Windows:  `%Appdata%\Roaming\.minecraft\contentpacks`
-   Linux:  `~/.minecraft/contentpacks`
-   Mac OS X:  `~/Library/Application Support/minecraft/contentpacks`

#### Explanations

!!! summary "Content Pack Root"
	A simple folder with all necessary resources below.  
	To be compiled as a **zip file**
	
___

!!! warning "content.pack" 
    The most important file to let **MJson** recognize the content pack  
	That's a **json** structured file.
	
```json
{
  "packName": "Ma Super Packy Pack", //mandatory
  "namespace": "super_pack", //mandatory
  "version": "0.0.1", //mandatory
  "authors" : ["ZeAmateis"], //optional
  "credits" : ["Thanks to my parents to bring me life."], //optional
  "description": [ //optional
    "That was ma super pack description !",
    "Yeah boiiii."
  ]
}
```
___

!!! warning "pack.mcmeta" 
	An other important file !	
	This file is mandatory in resources packs, so it's mandatory for content packs.  
	**MJson** can recognize what **assets** to be loaded  
	The **json** structure is the same as Resources Packs
	
___

!!! note "pack.png"
	An optional logo to pimp your content pack
___

!!! summary "assets"
	The main **folder** to include all resources of your content pack  
	Textures, json models, sounds, etc  
	Like a basic resource pack !
___
!!! summary "objects"
	The main **folder** to include all new objects json datas.  
	Theses datas is needed to implements new objects in the game
___

!!! note "blocks.json"
	**Json file** to register all new blocks to be implemented in the game  
	<u>If `Array` in file is empty or file does not exist, the file is ignored</u>

<details>
  <summary>Exemple json structure</summary>
  
```json
[
  {
    "registryName": "test",
    "itemGroup": "super_pack:blocks",
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
      "tickingRandomly": false,
      "doesNotBlockMovement": false
    },
    "voxelShape": {
      "shape": {
        "x1": 1,
        "y1": 0,
        "z1": 1,
        "x2": 15,
        "y2": 16,
        "z2": 15
      },
      "collisionShape": {
        "x1": 1,
        "y1": 0,
        "z1": 1,
        "x2": 15,
        "y2": 15,
        "z2": 15
      }
    }
  },
  {
    "registryName": "test_2",
    "itemGroup": "super_pack:blocks"
  }
]
```

</details>

___

!!! note "items.json"
	**Json file** to register all new items to be implemented in the game  
	<u>If `Array` in file is empty or file does not exist, the file is ignored</u>

> W.I.P
___

!!! note "itemgroup.json"
	**Json file** to create a new creative tab to add your fresh new objects inside !

<details>
	<summary>Exemple json structure</summary>

```json
{
  "id": "super_pack:blocks",
  "icon": "super_pack:test",
  "noTitle": false,
  "hasSearchBar": true,
  "hasScrollBar": false
}
```

</details>

___