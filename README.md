# myDV · RayNeo X3 Pro 适配版

这是 **雷鸟 RayNeo X3 Pro 眼镜专用的 myDV 非官方适配及 Release 发布仓库**，fork 自 [mytv-android/myDV](https://github.com/mytv-android/myDV)。原应用由上游开发，本仓库维护眼镜适配版的下载和版本说明。

## 下载

**[下载最新适配版](https://github.com/WayneShao/myDV-X3Pro/releases/latest)**

| 版本 | 下载与说明 |
|---|---|
| 2.1.37 | [Release](https://github.com/WayneShao/myDV-X3Pro/releases/tag/x3pro-v2.1.37) |
| 2.1.36 | [Release](https://github.com/WayneShao/myDV-X3Pro/releases/tag/x3pro-v2.1.36) |
| 2.1.35 | [Release](https://github.com/WayneShao/myDV-X3Pro/releases/tag/x3pro-v2.1.35) |
| 2.0.33 | [Release](https://github.com/WayneShao/myDV-X3Pro/releases/tag/x3pro-v2.0.33) |
| 2.0.32 | [Release](https://github.com/WayneShao/myDV-X3Pro/releases/tag/x3pro-v2.0.32) |
| 2.0.31 | [Release](https://github.com/WayneShao/myDV-X3Pro/releases/tag/x3pro-v2.0.31) |
| 1.5.30 | [Release](https://github.com/WayneShao/myDV-X3Pro/releases/tag/x3pro-v1.5.30) |

从 2.1.37 起，每个 Release 同时提供 **无语音版**（`-no-voice.apk`，内置双目拼音输入法）和 **完整版**（`-debug.apk`，另含离线语音）。两者同签名、同包名，可保留数据覆盖切换，不可并存。应用内更新保持当前类型；2.1.36 的旧更新器会选择完整版。

进入对应 Release，下载 Assets 中的 APK。`SHA256SUMS.txt` 用于核对文件完整性。

## X3 Pro 适配内容

- 应用页面、设置、弹窗、菜单及 Toast 的双目显示适配。
- 视频沿用现有 TextureView 双目显示路径，保留字幕和控制界面。
- 右触控板使用原生焦点“光标模式”：上下左右滑动对应方向键，单击确认，双击返回，双指轻触打开选项菜单。
- 左触控板保留系统音量操作，不进入应用导航。
- 焦点恢复及导航时自动弹出输入法的抑制；从 2.1.37 起接入应用内双目拼音输入，不替换系统输入法。
- 从 2.1.36 起，自动检查和手动检查更新均指向本仓库，只接受同签名的 X3 Pro 适配 APK；安装仍需用户确认。

“光标模式”指移动界面的选中框，不是移动鼠标小白点。各版本的构建、安装和实机验证范围见 Release 说明；不把旧版本的体验视为新版本全部功能已验收。

## 安装与升级

**从旧适配版升级：请先手动下载安装最新适配版一次。** 旧版关闭了更新入口；安装本版后，可通过应用内检查更新获取后续 X3 Pro 版本。更新包检查 SHA256、包名、递增版本号和适配签名。

本仓库已发布版本使用同一适配签名，已有同签名适配版可覆盖升级并保留数据。适配签名与上游原版不同：若设备已安装官方原版，直接覆盖会发生签名冲突，请先保留配置，再决定迁移方式。

文件名中的 `debug` 是既有交付命名，发布的 APK 均已签名并检查。适配签名证书 SHA-256：

```text
4c18f1a5584e01efded17bc5303a9f3c3912ded59b88722261ff2a912172d4d9
```

## 反馈与上游

眼镜双目显示、镜腿手势和焦点适配问题请在[本仓库 Issues](https://github.com/WayneShao/myDV-X3Pro/issues)反馈，注明版本、设备和操作步骤。原应用功能介绍保留在 [上游说明](README.upstream.md)，原项目见 [mytv-android/myDV](https://github.com/mytv-android/myDV)。

本 fork 主要用于适配包发布，不包含完整 Android 应用源码；当前上游公开仓库也未提供完整应用源码。保留上游 [LICENSE](LICENSE) 与作者归属。本仓库的 Release 与上游官方 Release 独立管理，继承的自动化工作流已禁用。
