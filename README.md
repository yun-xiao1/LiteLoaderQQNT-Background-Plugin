<p align="center">
  <img width="160" height="160" alt="icon" src="./icon.png" />
</p>

<h1 align="center">背景插件 Background Plugin</h1>

<p align="center">
  <a href="/LICENSE"><img src="https://img.shields.io/github/license/yun-xiao1/LiteLoaderQQNT-Background-Plugin" alt="LICENSE"></a>
  <a href="https://github.com/yun-xiao1/LiteLoaderQQNT-Background-Plugin"><img src="https://img.shields.io/badge/fork-yun--xiao1%2FBackground--Plugin-blue" alt="Fork"></a>
</p>

LiteLoaderQQNT 插件，用于在 QQNT 聊天界面展示背景图片或视频，并对部分 QQNT 界面做透明化/毛玻璃处理。

LiteLoaderQQNT 本体：[LiteLoaderQQNT](https://github.com/mo-jinran/LiteLoaderQQNT)

> [!CAUTION]
> 不要在国内平台宣传该插件。不要在 QQ 官方群聊发送任何可以看出你使用了第三方插件的截图。

## Fork 说明与许可证

这是 `yun-xiao1/LiteLoaderQQNT-Background-Plugin` 的维护 fork，基于原项目 `xh321/LiteLoaderQQNT-Background-Plugin` 修改。

本 fork 遵守原项目的 MIT 许可证，并在源码与发布包中保留原作者版权声明和完整许可协议：

- 原作者：`XiaoHe321`
- 原项目：`xh321/LiteLoaderQQNT-Background-Plugin`
- 当前 fork：`yun-xiao1/LiteLoaderQQNT-Background-Plugin`
- 许可证：`MIT`
- 许可协议全文：见仓库中的 `LICENSE` 文件

## 已知可用环境

当前版本主要按以下环境处理和测试：

| 项目 | 版本 |
| --- | --- |
| QQNT | `9.9.20-37051` x64 |
| LiteLoaderQQNT | `1.2.4` |
| 背景插件 | `0.2.25` |
| 系统 | Windows |

`manifest.json` 仍保留 `win32`、`darwin`、`linux` 平台声明，但本 fork 的修复主要针对 Windows QQNT 旧版环境。其他 QQNT 或 LiteLoaderQQNT 版本如果界面结构变化较大，可能仍会有兼容问题。

## 当前改动

- `manifest.json` 的仓库信息已改为 `yun-xiao1/LiteLoaderQQNT-Background-Plugin`，避免插件更新入口指回原仓库。
- 修复开启“是否对部分组件启用毛玻璃模糊效果”后，点击聊天输入区截图/文件按钮导致菜单或界面位置异常的问题。
- 毛玻璃效果不再作用到聊天输入区、输入工具栏和文件按钮浮层相关区域，避免影响截图/文件菜单渲染。
- 将 `.normal-file` 的毛玻璃范围收窄到聊天消息内容里的文件卡片，避免误影响文件按钮或文件浮层。
- 取消对 `.chat-func-bar` 高度的强制修改，避免打开截图/文件菜单时输入工具栏重新布局。

## 功能概览

- 支持本地文件夹随机轮播背景图片或视频。
- 支持选择单个本地图片/视频作为背景。
- 支持从网络 API 获取背景图片或视频。
- 支持按配置间隔自动切换背景。
- 支持多个 QQ 窗口共用同一背景。
- 支持保存最近一次 API 背景图。
- 支持对部分界面组件启用透明化与毛玻璃模糊效果。
- 支持媒体预览器背景生效开关。

## 下载与安装

正式包：

- GitHub 官方下载：[Background.zip](https://github.com/yun-xiao1/LiteLoaderQQNT-Background-Plugin/releases/download/0.2.25/Background.zip)
- SHA256 校验：[Background.zip.sha256](https://github.com/yun-xiao1/LiteLoaderQQNT-Background-Plugin/releases/download/0.2.25/Background.zip.sha256)

备用下载：

- 镜像 1：[gh.llkk.cc](https://gh.llkk.cc/https://github.com/yun-xiao1/LiteLoaderQQNT-Background-Plugin/releases/download/0.2.25/Background.zip)
- 镜像 2：[gh-proxy.com](https://gh-proxy.com/https://github.com/yun-xiao1/LiteLoaderQQNT-Background-Plugin/releases/download/0.2.25/Background.zip)

备用镜像不保证长期可用。如果镜像下载失败，请换回 GitHub 官方下载或稍后重试。

安装方法：

1. 下载上面的 `Background.zip`。
2. 打开 LiteLoaderQQNT 插件管理页面。
3. 导入插件压缩包，或将压缩包内容解压到 LiteLoaderQQNT 数据目录的 `plugins/background_plugin`。
4. 重启 QQNT。

如果已经安装过背景插件，建议先备份原 `background_plugin` 插件目录，再覆盖新版。

## 配置说明

启动 QQNT 后，插件会在 LiteLoaderQQNT 数据目录下创建背景插件配置与资源目录。

常用配置：

- `本地背景文件夹路径`：选择用于随机轮播的图片或视频目录。
- `本地背景文件路径`：选择单个图片或视频作为固定背景。
- `网络背景 API`：从网络接口读取背景图片或视频。
- `API JSON 路径`：当接口返回 JSON 时，用于指定图片/视频地址字段。详细说明见 `API-JSON路径帮助.md`。
- `自动更新背景图间隔`：设置自动切换背景的时间间隔。
- `是否多个窗口共用一个背景图`：多个 QQNT 窗口使用同一张背景。
- `是否对部分组件启用毛玻璃模糊效果`：对聊天气泡、侧栏等部分区域启用毛玻璃效果。
- `是否对媒体预览器生效背景`：控制图片预览器等媒体页面是否使用背景。

支持的常见图片格式：

```text
JPG, JPEG, PNG, BMP, APNG, WEBP, AVIF, GIF
```

支持的常见视频格式：

```text
MP4, WEBM, OGG
```

视频能否播放取决于 QQNT 内置 Chromium 对编码格式的支持。

## 已知限制

- QQNT 界面 class 名经常随版本变化，升级 QQNT 后可能出现透明化、毛玻璃或按钮菜单异常。
- 和其他主题、透明化、CSS 注入类插件一起使用时，可能会出现透明度叠加或显示异常。
- 网络背景 API 的稳定性取决于接口本身，接口失效、限流或返回结构变化都会导致背景无法更新。
- 视频背景会比图片背景占用更多资源，低配置设备可能出现卡顿。
- 从很旧的版本升级时，旧配置可能需要手动迁移到 LiteLoaderQQNT 数据目录下的 `background` 文件夹。

## 手动打包

```powershell
npm install --omit=dev
New-Item -ItemType Directory -Force -Path dist | Out-Null
Compress-Archive -Path manifest.json,main.js,preload.js,renderer.js,rangesServer.js,icon.png,package.json,package-lock.json,LICENSE,README.md,'API-JSON路径帮助.md',assets,node_modules -DestinationPath dist\Background.zip -Force
Get-FileHash dist\Background.zip -Algorithm SHA256
```

## 声明

- 本项目仅供学习和研究。
- 请勿用于非法用途。
- 本 fork 不代表原作者立场。
- 使用第三方插件可能带来账号或客户端风险，请自行判断并承担后果。
