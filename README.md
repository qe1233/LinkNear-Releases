# LinkNear 下载

LinkNear 是局域网聊天与文件传输应用。本仓库只用于公开分发，应用源码单独维护。

[下载最新版本](https://github.com/qe1233/LinkNear-Releases/releases/latest)

目前支持 Apple Silicon Mac。下载 Release 中的 `LinkNear-v版本号-macos-arm64.zip`，退出旧版并将 LinkNear.app 放入“应用程序”。请勿下载 GitHub 自动生成的 Source code 压缩包作为安装包。

v0.6.0 起可以通过侧栏“检查更新”下载更新，校验通过后点击“安装并重启”。旧版需手动覆盖安装一次。应用数据保存在本机，升级保留设备身份、联系人和聊天记录。

## 安全

- 更新包使用独立签名，应用内置公钥并在安装前验签，同时核对包内版本和应用身份。
- 正式 Release 开启不可变发布；本仓库关闭 Actions，不通过外部 PR 自动构建或发布。
- 检查更新访问 GitHub，但不上传聊天内容、联系人或文件。
- 当前为开发分发版本，尚未 Apple Developer ID 签名或公证；首次安装可能出现 macOS 安全提示。请勿为安装全局关闭 Gatekeeper。
- 发布签名代表来源和完整性，不保证软件不存在漏洞。首次安装请核对仓库所有者为 qe1233。

请勿在公开反馈中上传聊天记录、联系方式、身份密钥或包含私人信息的日志。
