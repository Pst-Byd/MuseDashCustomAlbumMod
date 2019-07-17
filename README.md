# MuseDash 自制谱面管理器

MushDash自制谱面管理器，支持在游戏内加载自制谱面



## 使用方法

使用**Visual Studio 2019**打开项目并生成

将生成的**MuseDashModManager.dll**与**0Harmony.dll**，以及

**Pathced_DLL**/中的Assembly_CSharp.dll复制到**MuseDash_Data/Managed/**文件夹中，覆盖原文件

**Resource/**中的**nocover.png**复制到**MuseDash_Data/StreamingAssets/**文件夹中

即可使用。



## 谱面制作方法

谱面为bms文件，可以使用iBMSC等编辑器编辑。

在游戏根目录的**maps**/中新建文件夹，文件夹名称随意(最好为你的曲目名称)。

文件夹中有以下文件：

- **cover.png** : 该谱面的封面文件，大小为440x440，如果没有则会使用默认封面。
- **\{文件夹名称\}\_map1.bms**，**\{文件夹名称\}\_map2.bms**，**\{文件夹名称\}\_map3.bms**对应了曲目的3个难度，由易到难。
- **\{名称\}.wav**或**\{名称\}.ogg**文件为谱面对应的歌曲(目前仅支持这两种格式)，\{名称\}由bms中的相关参数规定。
- 同时，可以选择剪辑曲目片段，存放为**\{名称\}\_demo.wav**或者**\{名称\}\_demo.ogg**文件(扩展名与完整歌曲名保持一致)，作为选择乐曲界面播放的音乐。如果没有则播放完整歌曲。



Resource文件中提供了一个简易的psd用于制作封面，以及一个示例bms文件。



## 问题报告

请提issue！



## 已知问题

- 在游玩自制谱面回到主界面可能会出现无法正常显示主界面歌曲。
- 收藏自定义曲目会导致整个存档损坏(已经屏蔽掉了收藏按钮，不要作死)
- 自定义曲面的封面会比原图略微糊一点
- 多语言时自定义曲面的文字显示不正确



## 使用库

[Harmony](https://github.com/pardeike/Harmony/)