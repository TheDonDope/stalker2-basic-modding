# 📚 Crude and brief tutorial of how to perform simple modding in S.T.A.L.K.E.R. 2: Heart of Chornobyl ☢️

## 🔨 Get the tools

- Fmodel [https://github.com/4sval/FModel/releases](https://github.com/4sval/FModel/releases "https://github.com/4sval/FModel/releases")
- unrealpak [https://github.com/btwOreO/unrealpak/archive/refs/heads/main.zip](https://github.com/btwOreO/unrealpak/archive/refs/heads/main.zip "https://github.com/btwOreO/unrealpak/archive/refs/heads/main.zip")
- AESDumpster [https://github.com/GHFear/AESDumpster](https://github.com/GHFear/AESDumpster)

## ⚒️ Do stuff

### 🔐 Get AES Keys

[https://forums.nexusmods.com/topic/13497429-aes-keys-guide/](https://forums.nexusmods.com/topic/13497429-aes-keys-guide/)


### 🗺️ Get the usmap file

[https://www.nexusmods.com/stalker2heartofchornobyl/mods/116?tab=files](https://www.nexusmods.com/stalker2heartofchornobyl/mods/116?tab=files)

## 📂 Extracting files

- Boot Fmodel
- Go to Directory at the top > AES key, write down the AES key.
- Go to Settings > Set Local Mapping File Enabled, and browse the mapping file there, point to the usmap file.
- In Settings, set the game UE version to UE5_1.
- Start browsing the paks files and using FModel: [https://github.com/Dmgvol/UE_Modding/blob/main/TheBasics/UsingFModel.md](https://github.com/Dmgvol/UE_Modding/blob/main/TheBasics/UsingFModel.md "https://github.com/Dmgvol/UE_Modding/blob/main/TheBasics/UsingFModel.md")
- Extract files you desire.

## 🔃 Modify the files the way you want

.cfg files are trival, just open them and edit the values. Textures, models and the like are harder to work with, as you need to cook the files once they are extracted in an empty UE project to generate uasset cooked files. Without the cooking, certain files won't be loaded by the game (if you find an uasset file in a pak, the file in your mod needs to be an uasset file, even though that uasset file might only contain a single png).

## 🗜️ Repak the files

- Make a folder named `MyModName_P`
- Copy the modified files in there with the full folder structure starting from `Stalker2` or `Engine`.
- Your mod should thus look like `MyModName_P/Stalker2/GameLite/GameData...`
- Drag and drop that folder on the unrealpak `UnrealPak-With-Compression.bat`, it will generate a .pak file.

## 💾 Loading the mod

- Add the pak file in the `S.T.A.L.K.E.R. 2 Heart of Chornobyl\Stalker2\Content\Paks\~mods` (create the `~mods` folder if it doesn't exist).

## 📑 Resources

- [https://buckminsterfullerene02.github.io/dev-guide/index.html](https://buckminsterfullerene02.github.io/dev-guide/index.html "https://buckminsterfullerene02.github.io/dev-guide/index.html") 
- [https://github.com/Dmgvol/UE_Modding](https://github.com/Dmgvol/UE_Modding "https://github.com/Dmgvol/UE_Modding") 
- [https://github.com/Buckminsterfullerene02/UE-Modding-Tools](https://github.com/Buckminsterfullerene02/UE-Modding-Tools "https://github.com/Buckminsterfullerene02/UE-Modding-Tools")