# LinkNear 下载

LinkNear 是局域网沟通与文件传输应用。本仓库用于公开分发，应用源码单独维护。

[查看最新版本](https://github.com/qe1233/LinkNear-Releases/releases/latest)

| 平台 | 当前版本 | 安装包 |
| --- | --- | --- |
| Apple Silicon Mac | v0.10.6 | [下载 ZIP](https://github.com/qe1233/LinkNear-Releases/releases/download/v0.10.6/LinkNear-v0.10.6-macos-arm64.zip) |
| Windows 10 / 11 x64 | v0.10.1 | [下载安装器](https://github.com/qe1233/LinkNear-Releases/releases/download/v0.10.1/LinkNear-windows-x64-setup.exe) |
| Android ARM64 | v0.10.6 | [下载 APK](https://github.com/qe1233/LinkNear-Releases/releases/download/v0.10.6/LinkNear-android-arm64.apk) |

Mac 解压后将 LinkNear.app 放入“应用程序”。Windows 运行安装器；若系统缺少 WebView2，安装器会获取 Microsoft 官方运行时。Android 使用系统安装器安装 APK。

Mac 和 Windows 可以通过侧栏“检查更新”下载安装新版，安装前会校验更新签名和包内版本。Android v0.10.4 起支持应用内检查更新、下载安装包并交由系统安装器确认覆盖升级，旧版可从官方发布页下载安装。升级保留设备身份、联系人和普通聊天记录。v0.10.1 起 Mac 与 Windows 使用独立更新通道，今后可分别发布；旧版可先通过兼容清单升级到 v0.10.1。

## v0.10.6 改进

- Mac 和 Android 新增“清理聊天记录”：按时间、会话与类别预览并确认清理，默认保留文件。
- 可选清理已接收文件：Mac 移至废纸篓，Android 删除应用拥有的接收文件。发送原件和临时会话受到保护。
- 保留联系人和群成员关系，防止旧消息重试后恢复已清理记录；不删除对方记录或已有备份。
- Windows 继续使用 v0.10.1，独立更新通道保持可用。

## v0.10.2 改进

- Mac 普通聊天通知按会话合并，连续消息减少重复弹出；读完或静音后清除。应用运行期间约一分钟后自动清理，侧栏未读数保留。
- Mac 和 Android 文字历史每批加载 30 条，单聊附件另按每批 30 条加载；打开显示最近消息，上滑再加载历史。
- 本次不重新构建 Windows，Windows 更新通道继续提供 v0.10.1。

## v0.10.1 改进

- 修复 Mac 高分屏拖拽文件与文件夹的落点判断，失败原因汇总提示。
- 大图片使用受控尺寸预览，原文件保持不变。
- 新增浅色、深色及跟随系统外观；打开会话显示最近记录，向上逐批加载历史。
- Android 10+ 普通接收文件保存到系统 Download/LinkNear；收到的文件夹保存为 ZIP。同名文件不覆盖，失败可重试；Android 7–9 仍使用应用私有目录。

公共下载文件在卸载后仍会保留。临时会话不导出至公共下载目录，继续使用隔离加密缓存。

## Android 范围

此前已完成 Android 15 ARM64 模拟器基础功能验收；v0.10.1 另通过下载目录、图片方向、视频 URI 和重启恢复等原生功能测试，尚未完成 vivo 实机验收。支持联系人、聊天、图片、视频、文件和单对单临时会话。视频使用原生播放器；临时视频按需从加密缓存读取，结束会话会关闭播放器。请在传输期间保持应用前台；首版暂不提供文件夹选择和系统回收站清理。

## 安全

- Mac 与 Windows 更新包使用独立签名。发布私钥保留在本机，私有仓库的 Windows Actions 仅手动构建，不持有签名私钥。
- Android APK 使用固定发布证书。后续覆盖升级由系统核对签名；[公开证书指纹](https://github.com/qe1233/LinkNear-Releases/releases/download/v0.10.6/android-signing-certificate.sha256)随安装包发布。
- 正式 Release 开启不可变发布；本分发仓库关闭 Actions。每次发布附带 SHA256SUMS.txt。
- 检查更新访问 GitHub，不上传聊天内容、联系人或传输文件。局域网沟通无需互联网。
- macOS 尚未使用 Apple Developer ID 签名或公证；Windows 尚未使用商业 Authenticode 证书，首次安装可能显示未知发布者提示。签名校验保证来源和完整性，不代表软件没有漏洞。

请在公开反馈中仅提供合成测试内容，避免上传私人聊天记录、联系方式或身份密钥。
