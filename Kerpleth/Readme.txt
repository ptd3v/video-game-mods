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


************************************************************************************************************************************************************************************
Mods文件目录说明

1、About文件夹（必要文件夹）
用于存放About.json文件和Preview.png文件，一个完整的Mod必须具备这两个文件，缺一不可。

*About.json：用于储存Mod作者、功能介绍等信息，它们将出现于该Mod的详情页（文件内有详细注释）
*Preview.png：该图片将作为封面出现于Mod的详情页。

2、Assemblies文件夹（可选）
  用于存放所有.dll格式的文件，客户端将读取这个文件夹里的.dll文件，并执行所有带有 [StaticConstructorOnStartup] 类的静态构造函数。

3、Sounds文件夹（可选）
  用于存放.wav格式的音乐文件，目前不支持其他音乐格式。 

4、Textures文件夹（可选）
用于存放.png格式的图片文件和“TextureInfos.json”文件，除.png外目前不支持其他的图片格式。
TextureInfos.json: 用于设置图片的锚点信息，文件内有详细注释。

5、Language文件夹（可选）
  用于存放ModLanguage.txt文件（不可修改文件名）。当客户端载入该Mod时，会将其内容合并到Keplerth_Data\StreamingAssets\Language\Language.txt文件中

6、Configs文件夹（可选）
用于存放所有.json格式的配置文件。文件名和配置内容可以参考Keplerth_Data\StreamingAssets\Config文件夹中的所有文件。
当客户端载入该Mod时，会将其相同名字的.json文件的内容合并到Keplerth_Data\StreamingAssets\Config中的.json文件中。
若Mod的.json文件内的ID与客户端的.json文件内的ID相同，则将它覆盖，若不同则新增。

