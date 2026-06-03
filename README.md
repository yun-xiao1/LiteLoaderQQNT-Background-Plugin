# LiteLoaderQQNT Background Plugin

这是 `yun-xiao1/LiteLoaderQQNT-Background-Plugin` 的维护 fork，基于原项目 `xh321/LiteLoaderQQNT-Background-Plugin` 修改。

插件用于在 QQNT 聊天界面展示背景图片或视频，并提供部分界面透明化/毛玻璃效果。

## 使用环境

当前维护版主要按下面环境处理和测试：

- QQNT：`9.9.20-37051` x64
- LiteLoaderQQNT：`1.2.4`
- 插件版本：`0.2.24`
- 系统：Windows

`manifest.json` 仍保留 `win32`、`darwin`、`linux` 平台声明，但本 fork 的修复主要针对 Windows QQNT 旧版环境。QQ 高版本如果界面结构变化较大，可能仍会有兼容问题。

## 本 fork 改动

- 插件仓库信息已改为 `yun-xiao1/LiteLoaderQQNT-Background-Plugin`。
- 修复开启“是否对部分组件启用毛玻璃模糊效果”后，点击聊天输入区截图按钮导致截图菜单显示异常的问题。
- 修复方式：毛玻璃效果不再作用到 `.chat-input-area` 和 `.main-area__footer`，避免影响截图菜单渲染；其它区域的毛玻璃效果保持不变。

## 安装方法

1. 下载本仓库 Release 中的 `Background.zip`。
2. 打开 QQ 的 LiteLoaderQQNT 插件管理页面。
3. 选择导入插件压缩包，导入 `Background.zip`。
4. 重启 QQ。

也可以使用插件商店类工具安装，但请确认插件来源指向本 fork：

`yun-xiao1/LiteLoaderQQNT-Background-Plugin`

## 配置说明

启动 QQ 后，插件会在 LiteLoaderQQNT 数据目录下创建背景插件配置与资源目录。

常用配置：

- 本地背景文件夹：选择用于轮播的图片或视频目录。
- 网络背景 API：从网络接口读取背景图片或视频。
- 自动轮播：按设置的时间间隔随机切换背景。
- 多窗口共用背景：多个 QQ 窗口使用同一背景。
- 毛玻璃模糊效果：对部分界面组件启用模糊效果。

支持的常见图片格式：

`JPG`、`JPEG`、`PNG`、`BMP`、`APNG`、`WEBP`、`AVIF`、`GIF`

支持的常见视频格式：

`MP4`、`WEBM`、`OGG`

视频能否播放取决于 QQNT 内置 Chromium 对编码的支持。

## 已知说明

- 和其它主题/透明化插件一起使用时，可能会出现透明度叠加或显示异常。
- 如果设置页面打不开、背景无法加载，先尝试在插件设置里恢复默认配置。
- 如果从很旧的版本升级，旧配置可能需要手动迁移到 LiteLoaderQQNT 数据目录下的 `background` 文件夹。

## 来源

- 原项目：`xh321/LiteLoaderQQNT-Background-Plugin`
- 当前 fork：`yun-xiao1/LiteLoaderQQNT-Background-Plugin`

## 协议

MIT
