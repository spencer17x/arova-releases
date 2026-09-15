# Arova Chrome 插件下载

[English](README.md) | **简体中文**

[下载最新版与历史版本](https://github.com/spencer17x/arova-releases/releases)

[功能介绍](FEATURES.zh-CN.md) · [完整使用指南](USAGE.zh-CN.md)

这是 Arova 官方公开下载仓库，用于分发编译后的 Chrome 插件安装包、SHA256 校验文件与版本信息。无需取得私有开发仓库权限，也无需从 Chrome 商店下载。

Arova 将 Fomo / Pump 动态集中到 XXYY、GMGN、DeBot 等支持的交易页面，提供账号备注、浏览器提醒和 Telegram 多目标通知。配置在插件独立管理页完成，浮窗用于查看通知与快捷操作。

插件支持中英文，默认跟随浏览器，可在管理页侧栏切换。Telegram 每个通知目标可独立选择中文或英文。

## 从这里开始

| 想做什么 | 查看文档 |
| --- | --- |
| 了解支持的平台与能力 | [功能介绍](FEATURES.zh-CN.md) |
| 安装或更新插件 | [安装与更新](USAGE.zh-CN.md#安装与更新) |
| 完成第一次配置 | [首次上手](USAGE.zh-CN.md#首次上手) |
| 连接 Fomo / Pump，开启服务端续期 | [监控授权](USAGE.zh-CN.md#连接监控来源)、[自动续期](USAGE.zh-CN.md#选择自动续期方式) |
| 设置 TG 群组/频道推送 | [Telegram 通知](USAGE.zh-CN.md#telegram-通知) |
| 查看付费、赠送或永久权益 | [方案与使用权](USAGE.zh-CN.md#方案与使用权) |
| 处理加载、登录或通知问题 | [常见问题](USAGE.zh-CN.md#常见问题) |

## 安装与更新

1. 在 Releases 中下载 `arova-chrome-版本.zip`，解压到准备长期保留的文件夹。
2. 打开 `chrome://extensions`，开启右上角的「开发者模式」。
3. 点击「加载已解压的扩展程序」，选择包含 `manifest.json` 的解压目录。
4. 点击 Arova 图标打开管理页，登录账号并完成所需配置。

更新时，将新包替换到原加载目录，在扩展管理页点击 Arova 的「重新加载」，再刷新交易页。不要先卸载，以保留浏览器设置。GitHub 安装包不会自动更新已安装的插件。

同名 Beta 版本可能重新构建；以 `release-info.json` 的构建标识与 `SHA256SUMS` 校验值区分新旧包。

## 版本内容

- `arova-chrome-版本.zip`：官方插件安装包。
- `SHA256SUMS`：安装包 SHA256。
- `release-info.json`：版本、构建标识、扩展 ID、生产接口及摘要。

固定扩展 ID：`gedflalfmklfccgaabdbcnjjchlfemfo`。

公开 tag 记录的是分发产物快照。GitHub 自动生成的 “Source code” ZIP/TAR 只包含本公开仓库的说明、发布配置和构建产物；安装请下载 `arova-chrome-版本.zip`。

此仓库不包含 Arova 的 TypeScript / Python 业务源码、服务端代码、私有 Git 历史、环境配置或密钥。Chrome 安装包包含运行必需的编译后 JavaScript。

## 许可

Arova 采用专有商业许可，见 [LICENSE](LICENSE)。公开下载不代表项目改为开源授权；第三方许可证与版权通知保留在安装包的 `THIRD_PARTY_NOTICES.txt` 中。账号使用权限和付费方案由 Arova 服务端决定。

[完整图文教程](USAGE.zh-CN.md#图文上手教程)
