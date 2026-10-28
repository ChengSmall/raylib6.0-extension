<img align="left" style="width:260px" src="https://github.com/raysan5/raylib/blob/master/logo/raylib_logo_animation.gif" width="288px">

**raylib 是一个简单易用的库，让你享受电子游戏编程的乐趣。**

raylib 深受 Borland BGI 图形库和 XNA 框架的启发，特别适合原型开发、工具制作、图形应用、嵌入式系统和教育领域。

*给冒险者的提示：raylib 是一个用于享受电子游戏编程乐趣的编程库；没有花哨的界面，没有可视化辅助工具，没有调试按钮……只有以最纯粹的斯巴达式程序员方式进行编码。*

准备好学习了吗？跳转到[代码示例！](https://www.raylib.com/examples.html)

---

<br>

[![GitHub Releases Downloads](https://img.shields.io/github/downloads/raysan5/raylib/total)](https://github.com/raysan5/raylib/releases)
[![GitHub Stars](https://img.shields.io/github/stars/raysan5/raylib?style=flat&label=stars)](https://github.com/raysan5/raylib/stargazers)
[![GitHub commits since tagged version](https://img.shields.io/github/commits-since/raysan5/raylib/6.0)](https://github.com/raysan5/raylib/commits/master)
[![GitHub Sponsors](https://img.shields.io/github/sponsors/raysan5?label=sponsors)](https://github.com/sponsors/raysan5)
[![Packaging Status](https://repology.org/badge/tiny-repos/raylib.svg)](https://repology.org/project/raylib/versions)
[![License](https://img.shields.io/badge/license-zlib%2Flibpng-blue.svg)](LICENSE)

[![Discord Members](https://img.shields.io/discord/426912293134270465.svg?label=Discord&logo=discord)](https://discord.gg/raylib)
[![Reddit Static Badge](https://img.shields.io/badge/-r%2Fraylib-red?style=flat&logo=reddit&label=reddit)](https://www.reddit.com/r/raylib/)
[![Youtube Subscribers](https://img.shields.io/youtube/channel/subscribers/UC8WIBkhYb5sBNqXO1mZ7WSQ?style=flat&label=Youtube&logo=youtube)](https://www.youtube.com/c/raylib)
[![Twitch Status](https://img.shields.io/twitch/status/raysan5?style=flat&label=Twitch&logo=twitch)](https://www.twitch.tv/raysan5)

[![Build Windows](https://github.com/raysan5/raylib/actions/workflows/build_windows.yml/badge.svg)](https://github.com/raysan5/raylib/actions/workflows/build_windows.yml)
[![Build Linux](https://github.com/raysan5/raylib/actions/workflows/build_linux.yml/badge.svg)](https://github.com/raysan5/raylib/actions/workflows/build_linux.yml)
[![Build macOS](https://github.com/raysan5/raylib/actions/workflows/build_macos.yml/badge.svg)](https://github.com/raysan5/raylib/actions/workflows/build_macos.yml)
[![Build WebAssembly](https://github.com/raysan5/raylib/actions/workflows/build_webassembly.yml/badge.svg)](https://github.com/raysan5/raylib/actions/workflows/build_webassembly.yml)

[![Build CMake](https://github.com/raysan5/raylib/actions/workflows/build_cmake.yml/badge.svg)](https://github.com/raysan5/raylib/actions/workflows/build_cmake.yml)
[![Build examples Windows](https://github.com/raysan5/raylib/actions/workflows/build_examples_windows.yml/badge.svg)](https://github.com/raysan5/raylib/actions/workflows/build_examples_windows.yml)
[![Build examples Linux](https://github.com/raysan5/raylib/actions/workflows/build_examples_linux.yml/badge.svg)](https://github.com/raysan5/raylib/actions/workflows/build_examples_linux.yml)

特性
--------
  - **无外部依赖**，所有必需的库都已[包含在 raylib 中](https://github.com/raysan5/raylib/tree/master/src/external)
  - 支持多个平台：**Windows、Linux、MacOS、RPI、Android、HTML5……以及更多！**
  - 使用纯 C 代码（C99）编写，采用 PascalCase/camelCase 命名法
  - 通过 OpenGL 实现硬件加速：**1.1、2.1、3.3、4.3、ES 2.0、ES 3.0**
  - **独特的 OpenGL 抽象层**（可作为独立模块使用）：[rlgl](https://github.com/raysan5/raylib/blob/master/src/rlgl.h)
  - **软件渲染器**后端（无需 OpenGL！）：[rlsw](https://github.com/raysan5/raylib/blob/master/src/external/rlsw.h)
  - 支持多种**字体**格式（TTF、OTF、FNT、BDF、精灵字体）
  - 支持多种纹理格式，包括**压缩格式**（DXT、ETC、ASTC）
  - **完整的 3D 支持**，包括 3D 形状、模型、公告板、高度图等！
  - 灵活的材质系统，支持经典贴图和 **PBR 贴图**
  - 支持**动画 3D 模型**（骨骼动画）（IQM、M3D、glTF）
  - 支持着色器，包括模型着色器和**后处理**着色器
  - **强大的数学模块**，用于向量、矩阵和四元数运算：[raymath](https://github.com/raysan5/raylib/blob/master/src/raymath.h)
  - 音频加载和播放，支持流式传输（WAV、QOA、OGG、MP3、FLAC、XM、MOD）
  - 支持**VR 立体渲染**，可配置 HMD 设备参数
  - 庞大的示例集合，包含[超过 140 个代码示例](https://github.com/raysan5/raylib/tree/master/examples)！
  - 提供[超过 70 种编程语言](https://github.com/raysan5/raylib/blob/master/BINDINGS.md)的绑定！
  - **免费且开源**

限制
-----------

raylib 出于代码简洁性的考虑，在设计上存在一些限制。有一些分支、替代方案和示例可用于克服其中大部分限制，但需要用户根据具体需求修改该库。

  - 默认情况下为单窗口、单 OpenGL 上下文，不支持多窗口
  - 在支持窗口的平台上，窗口缩放和移动会停止渲染循环
  - `RenderTextures` 在垂直方向上是翻转的（这是 OpenGL 提供的方式），需要用户自行绘制后再翻转显示到屏幕上
  - 字体光栅化质量低于使用 `Freetype2`、`HarfBuzz` 或 `Slug` 的替代方案
  - 文本绘制不支持 RTL、连字或表情符号

基础示例
--------------
这是一个基础的 raylib 示例，它创建一个窗口，并在屏幕中央绘制文本 `"Congrats! You created your first window!"`。可以在[这里查看该示例的网页实时运行版本](https://www.raylib.com/examples/core/loader.html?name=core_basic_window)。
```c
#include "raylib.h"

int main(void)
{
    InitWindow(800, 450, "raylib example - basic window");

    while (!WindowShouldClose())
    {
        BeginDrawing();
            ClearBackground(RAYWHITE);
            DrawText("Congrats! You created your first window!", 190, 200, 20, LIGHTGRAY);
        EndDrawing();
    }

    CloseWindow();

    return 0;
}
```

构建与安装
----------------------

raylib 的 Windows、Linux、macOS、Android 和 HTML5 二进制发行版可在 [GitHub Releases 页面](https://github.com/raysan5/raylib/releases)获取。

raylib 也可通过多个操作系统发行版上的多个包管理器获取。

#### 在多个平台上安装和构建 raylib

[raylib Wiki](https://github.com/raysan5/raylib/wiki#development-platforms) 包含在多个平台上构建和使用的详细说明。

 - [在 Windows 上工作](https://github.com/raysan5/raylib/wiki/Working-on-Windows)
 - [在 macOS 上工作](https://github.com/raysan5/raylib/wiki/Working-on-macOS)
 - [在 GNU Linux 上工作](https://github.com/raysan5/raylib/wiki/Working-on-GNU-Linux)
 - [在 Chrome OS 上工作](https://github.com/raysan5/raylib/wiki/Working-on-Chrome-OS)
 - [在 FreeBSD 上工作](https://github.com/raysan5/raylib/wiki/Working-on-FreeBSD)
 - [在 Raspberry Pi 上工作](https://github.com/raysan5/raylib/wiki/Working-on-Raspberry-Pi)
 - [为 Android 工作](https://github.com/raysan5/raylib/wiki/Working-for-Android)
 - [为 Web（HTML5）工作](https://github.com/raysan5/raylib/wiki/Working-for-Web-(HTML5))
 - [使用 CMake 在任何地方工作](https://github.com/raysan5/raylib/wiki/Working-with-CMake)

*请注意，Wiki 开放编辑。如果你在为你的目标平台构建 raylib 时发现问题，欢迎编辑 Wiki 或提交相关 issue。*

#### 在多个 IDE 中配置 raylib

raylib 是在 Windows 平台上使用 [Notepad++](https://notepad-plus-plus.org/) 和 [MinGW GCC](https://www.mingw-w64.org/) 编译器开发的，但它也可以与多个平台上的其他 IDE 一起使用。

[Projects 目录](https://github.com/raysan5/raylib/tree/master/projects)包含多个可直接使用的**项目模板**，用于在多个 IDE 中构建 raylib 和代码示例。

*请注意，支持的 IDE 很多，部分提供的模板可能需要检查，因此如果你发现某个模板有问题，或者认为它们可以改进，欢迎提交 PR 或提交相关 issue。*

学习与文档
------------------

raylib 的设计目标是使用[示例](https://github.com/raysan5/raylib/tree/master/examples)作为主要参考来学习。没有标准的 API 文档，但有一份[**速查表**](https://www.raylib.com/cheatsheet/cheatsheet.html)，其中包含该库所有可用函数，以及对每个函数的简短描述，输入参数和返回值名称应该足够直观，便于理解每个函数的工作方式。

关于 raylib 设计的其他文档可以在 [raylib GitHub Wiki](https://github.com/raysan5/raylib/wiki) 中找到。以下是相关链接：

 - [raylib 速查表](https://www.raylib.com/cheatsheet/cheatsheet.html)
 - [raylib 架构](https://github.com/raysan5/raylib/wiki/raylib-architecture)
 - [raylib 库设计](https://github.com/raysan5/raylib/wiki)
 - [raylib 示例集合](https://github.com/raysan5/raylib/tree/master/examples)
 - [raylib 游戏集合](https://github.com/raysan5/raylib-games)


联系与网络
---------------------

raylib 出现在多个网络平台上，raylib 社区每天都在发展壮大。如果你正在使用 raylib 并享受它，欢迎加入我们的任何网络平台。最活跃的网络平台是我们的 [Discord 服务器](https://discord.gg/raylib)！ :)

 - 网页：[https://www.raylib.com](https://www.raylib.com)
 - Discord：[https://discord.gg/raylib](https://discord.gg/raylib)
 - X：[https://x.com/raysan5](https://x.com/raysan5)
 - BlueSky：[https://bsky.app/profile/raysan5](https://bsky.app/profile/raysan5.bsky.social)
 - Twitch：[https://www.twitch.tv/raysan5](https://www.twitch.tv/raysan5)
 - Reddit：[https://www.reddit.com/r/raylib](https://www.reddit.com/r/raylib)
 - Patreon：[https://www.patreon.com/raylib](https://www.patreon.com/raylib)
 - YouTube：[https://www.youtube.com/channel/raylib](https://www.youtube.com/c/raylib)

贡献者
------------

<a href="https://github.com/raysan5/raylib/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=raysan5/raylib&max=800&columns=24&anon=0" />
</a>

许可证
-------

raylib 采用未修改的 zlib/libpng 许可证授权，这是一个经 OSI 认证、类似 BSD 的许可证，允许与闭源软件进行静态链接。更多详情请查看 [LICENSE](LICENSE)。

raylib 内部使用了一些库来进行窗口/图形/输入管理，并支持不同文件格式的加载；所有这些库都已内嵌，并可在 [src/external](https://github.com/raysan5/raylib/tree/master/src/external) 目录中获取。详情请查看 [raylib Wiki](https://github.com/raysan5/raylib/wiki) 上的 [raylib 依赖许可证](https://github.com/raysan5/raylib/wiki/raylib-dependencies)。