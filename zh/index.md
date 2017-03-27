---
layout: default
ref: index
lang: 中文
---

宁芙是一个可用于GNU/Linux的输入法框架。 宁芙具有基于模块的客户端 - 服务器结构，在其中应用程序充当客户端，并通过**Unix套接字**与宁芙服务器**同步**通信。

## 轻量级

为了减少了内存占用，宁芙作为一个**单例模式**。
如果需要，宁芙可以作为多个实例模式。
`nimf-daemon`处理宁芙协议和XIM协议。

## 宁芙提供:

* 输入法服务器
  * `nimf-daemon`
* 语言引擎
  * 中文（Alpha阶段，基于sunpinyin，libchewing，librime）
  * 日语（Alpha阶段，基于anthy）
  * 韩语（基于libhangul）
* 服务模块
  * 指示器（基于appindicator）
  * Wayland
  * XIM（基于IMdkit）
* 客户端模块
  * GTK+2, GTK+3, Qt4, Qt5
* 设置工具配置宁芙
  * `nimf-settings`
* 开发文件
  * C库和头文件

## 许可证

宁芙是自由软件：您可以根据自由软件基金会发布的GNU宽通用公共许可证（版本3或许可证的任何更新版本）重新分发和/或修改它。

宁芙是分发的，希望它将是有用的，**但没有任何保证；甚至没有对适销性或适用于特定用途的默示保证。**

有关更多详细信息，请参阅GNU宽通用公共许可证。

您应该收到了GNU宽通用公共许可证的副本连同本程序; 如果没有，请参见<http://www.gnu.org/licenses/>。
