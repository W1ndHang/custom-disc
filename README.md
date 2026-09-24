# Custom Disc

![Minecraft](https://img.shields.io/badge/Minecraft-1.21.1-brightgreen)

![Loader](https://img.shields.io/badge/Loader-Fabric-informational)

![Environment](https://img.shields.io/badge/Environment-Client%20%26%20Server-blueviolet)

![License](https://img.shields.io/badge/License-Proprietary-lightgrey)

[English](#english) · [中文](#中文)

**Download:** [Modrinth](https://modrinth.com/mod/custom-disc) · [GitHub Releases](https://github.com/W1ndHang/custom-disc/releases)

Custom Disc turns your own audio files into real in-game music discs — import an MP3, WAV or OGG and play it in a jukebox, or in the new Jukebox Minecart.

把你自己电脑里的音频文件变成游戏里真正的唱片——导入 MP3、WAV 或 OGG，放进唱片机播放，或者用新的「唱片机矿车」。

---

## Screenshots / 截图

>

> **[Screenshot 2 — to add]** The two crafting recipes: Blank Disc and Jukebox Minecart.  
> **[截图 2 —— 待补]** 两个合成配方：空白唱片、唱片机矿车。

> **[Screenshot 3 — to add]** A jukebox playing a custom disc, with note particles.  
> **[截图 3 —— 待补]** 唱片机正在播放自定义唱片，带音符粒子。

> **[Screenshot 4 — to add]** The Jukebox Minecart playing while moving along rails.  
> **[截图 4 —— 待补]** 唱片机矿车在铁轨上边行驶边播放。

> **[Screenshot 5 — to add]** A written disc's tooltip, showing its `id` and `signal`.  
> **[截图 5 —— 待补]** 音乐唱片的提示框，显示 `id` 与 `signal`。

---

## English

### What it is

Custom Disc is a Fabric mod for Minecraft 1.21.1 that lets you import your own audio files and use them as music discs. It does not rely on resource packs or on replacing vanilla files: the audio you import is stored by the world itself, so any disc you create keeps working after a restart, and other players on the same server hear it too.

### Features

- **Import your own audio** — MP3, WAV and OGG, up to 64 MB per file, chosen through a file picker inside the game.
- **Playback range and falloff** — set how far the disc can be heard (16–256 blocks) and where it starts fading out (0–128 blocks).
- **Looping** — play once, or loop indefinitely with an optional pause between repeats (0–60 seconds).
- **Jukebox Minecart** — a jukebox on rails. Not rideable, plays while it moves, and drops its disc when emptied or broken.
- **Redstone output** — a comparator behind a jukebox reads a per-disc signal value (0–15), so discs can be told apart by a circuit.
- **Note particles** — playing discs emit the familiar note particles; the minecart's particles drift behind it as it travels.
- **Underwater acoustics** — sound is low-pass filtered and fades faster while you are submerged.
- **Follows the vanilla volume slider** — discs use the **Jukebox/Note Blocks** volume from *Options → Music & Sounds*, the same slider that controls vanilla music discs, so you can turn all of them down together.
- **Three languages** — English, 简体中文 and Français.

### Requirements

|            |                                                   |
| ---------- | ------------------------------------------------- |
| Minecraft  | 1.21.1                                            |
| Mod loader | Fabric Loader 0.15.0 or newer                     |
| Dependency | [Fabric API](https://modrinth.com/mod/fabric-api) |
| Java       | 21 or newer                                       |

### Installation

1. Install Fabric Loader for Minecraft 1.21.1.
2. Put Fabric API and `custom_disc-1.0.0.jar` into your `mods` folder.
3. Launch the game.

For a multiplayer server, install the mod on **both** the client and the server. They must run the **same version** of the mod: it sends its own network packets, so mismatched versions cannot connect.

### How to use

1. **Craft a Blank Disc** — 4 Blackstone in a cross shape, with 1 Redstone Dust in the centre.
2. **Import audio** — hold the Blank Disc and **sneak + right-click** to open the import window. Choose your file, type a name for the disc, and set the range, falloff, looping and loop delay. Press Confirm.
3. **Play it** — right-click a vanilla Jukebox while holding the disc. Right-click again to stop and eject.
4. **Or use the Jukebox Minecart** — craft one from a Jukebox and a Minecart, place it on rails, then right-click it with a disc to insert it. Right-click with an empty hand to eject. It cannot be ridden.

The disc's tooltip shows its internal `id` and its redstone `signal` value.

### Notes and limitations

- Imported audio is stored per world, on the server, at `<world folder>/custom_disc/discs/<id>.dat`. The import window runs on your client, but the file is written by the server — on a server, the disc belongs to the server's world.
- **Range and falloff only apply to mono audio.** Stereo files play at full volume everywhere.
- Each disc is given a fixed redstone signal value when it is created, and it does not change afterwards.
- A large file (up to 64 MB) takes a moment to transfer when it starts playing.

### Reporting bugs

Please use the [issue tracker](https://github.com/W1ndHang/custom-disc/issues) and fill in the bug report form. It asks for your mod version, Minecraft version, Fabric API version, whether you are in singleplayer or on a server, and your `latest.log`. Those details are what make a bug reproducible.

### Credits

- MP3 decoding uses **JLayer 1.0.1** by JavaZOOM, licensed under the **LGPL**. It is bundled unmodified as a nested jar and is not covered by this project's license.
- OGG decoding uses **stb_vorbis** through LWJGL, which ships with Minecraft.
- This is a third-party modification. It is not an official Minecraft product and is not associated with Mojang Studios or Microsoft.

### License

All rights reserved. You may redistribute **unmodified** copies free of charge, including inside a free modpack. You may not modify, repackage, rename, decompile or sell it. See [LICENSE](LICENSE) for the full terms.

---

## 中文

### 这是什么

Custom Disc 是一个面向 Minecraft 1.21.1 的 Fabric 模组，让你把**自己电脑里的音频文件**导入游戏，当作音乐唱片使用。它不依赖资源包，也不替换原版文件：导入的音频由存档自己保存，所以重启后唱片依然可用，同一个服务器上的其他玩家也能听见。

### 功能

- **导入你自己的音频** —— 支持 MP3、WAV、OGG，单个文件最大 64 MB，在游戏内通过文件选择框挑选。
- **播放半径与衰减** —— 设定唱片能传多远（16–256 格），以及从多远开始淡出（0–128 格）。
- **循环播放** —— 只播一次，或者无限循环，并可设置每次循环之间的间隔（0–60 秒）。
- **唱片机矿车** —— 一个会跑的唱片机。不能乘坐，行驶途中持续播放，取出唱片或破坏时会掉落唱片。
- **红石输出** —— 唱片机后方放比较器可读出每张唱片各自的信号强度（0–15），可以用电路区分不同唱片。
- **音符粒子** —— 播放中的唱片会飘出熟悉的音符粒子；矿车行驶时粒子会往后飘。
- **水下音效** —— 玩家潜水时声音会被低通滤波，且衰减更快。
- **跟随原版音量条** —— 唱片用的&#x662F;**「选项 → 音乐和声音」里「唱片机／音符盒」**&#x90A3;一格音量，和原版唱片共用同一条，可以一起调低。
- **三种语言** —— 英文、简体中文、法文。

### 运行要求

|           |                                                   |
| --------- | ------------------------------------------------- |
| Minecraft | 1.21.1                                            |
| 模组加载器     | Fabric Loader 0.15.0 或更新                          |
| 前置依赖      | [Fabric API](https://modrinth.com/mod/fabric-api) |
| Java      | 21 或更新                                            |

### 安装

1. 为 Minecraft 1.21.1 安装 Fabric Loader。
2. 把 Fabric API 与 `custom_disc-1.0.0.jar` 放进 `mods` 文件夹。
3. 启动游戏。

**联机服务器**：客户端和服务端**都要装**，而且必须是**同一个版本**。这个模组使用自己的网络包，版本不一致会直接连不上。

### 使用方法

1. **合成空白唱片** —— 4 个黑石摆成十字，中间放 1 个红石粉。
2. **导入音频** —— 手持空白唱片，**潜行 + 右键**打开导入界面。选择文件、填写唱片名称，再设置半径、衰减、是否循环与循环间隔，点「确定」。
3. **播放** —— 手持唱片右键点击原版唱片机即可插入播放，再次右键停止并弹出唱片。
4. **或者用唱片机矿车** —— 用一个唱片机加一个矿车合成，放到铁轨上，手持唱片右键插入。空手右键弹出。它不能乘坐。

唱片的提示框会显示它的内部 `id` 和红石 `signal` 值。

### 注意事项与限制

- 导入的音频按**存档**保存在服务端，路径为 `<存档目录>/custom_disc/discs/<id>.dat`。导入界面在客户端运行，但文件由服务端写入——在服务器上，唱片属于服务器的存档。
- **播放半径与衰减只对单声道音频生效。** 立体声文件在任何位置都是满音量播放。
- 每张唱片在创建时就被赋予一个固定的红石信号值，之后不会改变。
- 大文件（最大 64 MB）在开始播放时需要一点传输时间。

### 反馈问题

请到 [issue 反馈区](https://github.com/W1ndHang/custom-disc/issues) 填写问题表单。表单会问你的模组版本、Minecraft 版本、Fabric API 版本、单机还是联机，以及 `latest.log` 日志——有这些才可能定位问题。

### 致谢

- MP3 解码使用 JavaZOOM 的 **JLayer 1.0.1**，其许可证为 **LGPL**。它以未修改的嵌套 jar 形式打包，不受本项目的许可条款约束。
- OGG 解码通过 LWJGL 的 **stb_vorbis** 实现，LWJGL 随 Minecraft 一同提供。
- 这是第三方模组，不是 Minecraft 官方产品，与 Mojang Studios 及微软无关。

### 许可

保留所有权利。你可以**免费转发未经修改的**副本，包括放进免费整合包；但不得修改、重新打包、改名、反编译或售卖。完整条款见 [LICENSE](LICENSE)。
