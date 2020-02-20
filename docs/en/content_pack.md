# Content Pack

### Content Pack Files Structure
First at all, you need to understand the content pack files hierarchy.  

#### Folder/Zip File Structure
```
📁 Content Pack Root
├─	📝 content.pack
├─	📝 pack.mcmeta    
├─	🖼️ pack.png
│
├── 📁 assets
│   
└── 📁 objects
    ├─  📁 biomes
	├─	📁 blocks
	├─	📁 effects
	├─	📁 events
    │   └── 📁 blocks
	├─	📁 generations
    │   └── 📁 ores
	├─	📁 itemgroup
    ├─	📁 items
	├─	📁 materials
    │   ├─  📁 armor
    │   └── 📁 tools
	├─	📁 paintings
	├─	📁 potions
	└─	📁 sounds
```

#### Content Pack folder/zip file directory
-   Windows:  `%Appdata%\Roaming\.minecraft\contentpacks`
-   Linux:  `~/.minecraft/contentpacks`
-   Mac OS X:  `~/Library/Application Support/minecraft/contentpacks`

### Explanations

!!! summary "Content Pack Root"
	A simple folder with all necessary resources below.  
	To be compiled as a **zip file** or **directly a folder**
	
___

#### content.pack

!!! warning "content.pack" 
    The most important file to let **Nuwa** recognize the content pack  
	That's a **json** structured file.
	
```json
{
  "packName": "Ma Super Packy Pack", //mandatory
  "namespace": "super_pack", //mandatory
  "version": "0.0.1", //mandatory
  "nuwaDataVersion" : 2, //mandatory
  "authors" : ["ZeAmateis"], //optional
  "credits" : ["Thanks to my parents to bring me life."], //optional
  "description": [ //optional
    "That was ma super pack description !",
    "Yeah boiiii."
  ]
}
```

!!! tip  
    You can implement a Creative Commons licence for your work if you want.
    See [Work with licenses](license/license.md) section.
___

#### pack.mcmeta

!!! warning "pack.mcmeta" 
	An other important file !	
	This file is mandatory in resources packs, so it's mandatory for content packs.  
	**Nuwa** can recognize what **assets** to be loaded  
	The **json** structure is the same as Resources Packs
	
	!!! tip "[Check structure on Minecraft Wiki](https://minecraft.gamepedia.com/Resource_pack#Contents)"
___

#### pack.png

!!! note "pack.png"
	An optional logo to pimp your content pack
___

#### assets

!!! summary "assets"
	The main **folder** to include all resources of your content pack  
	Textures, json models, sounds, etc  
	Like a basic resource pack !
___

#### data

!!! summary "data"
	The main **folder** to include all data of your content pack  
	loot_tables, tags, etc 
	Like a basic resource pack !
___

#### objects

!!! summary "objects"
	The main **folder** to include all new objects json datas.  
	Theses datas is needed to implements new objects in the game
___