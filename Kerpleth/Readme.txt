Directory structure of a mod folder


1. "About" (compulsory): 
This folder should have the following two files:
   1) An "About.json" file – is used to store information such as the name of the mod author, description of the mod and etc.  This will be shown on your Steam Workshop page (more are explained in "Mods\Example\About\ About.json" file).
   2)A "Preview.png" file – this will be the preview image of the mod.

2. "Assemblies" (optional):
For storing .dll files. 
It will read all the .dll files when the game starts, and execute all static constructors with the [StaticConstructorOnStartup] class.

3. "Sounds" (optional):
For storing music files. (.wav is currently the only supported format)

4. "Textures" (optional):
For storing image files. (.png is currently the only supported format)
The "TextureInfos.json" file is used to configure the pivot points of images stored in Textures folder.

5. "Language" (optional):
For storing the language file "ModLanguage.txt". (It must be in this name)
The content of the language file (i.e. ModLanguage.txt) will be updated to "StreamingAssets\Language\Language.txt" file when the mod is implemented to the game.

6. "Configs" (optional):
For storing all configuration files (.json format)
File name and file contents can refer to the files in "Keplerth_Data\StreamingAssets\Config". 
If the configuration files in this folder have the same name as the ones in "Keplerth_Data\StreamingAssets\Config", 
then the data will be updated to the files in "StreamingAssets\Config" when the game starts.
If the ID used in the configuration file in this folder is the same as the one used in configuration file in "StreamingAssets\Config" folder, 
then the data will be overwritten. If different IDs are used, then it will be added as a new data.
