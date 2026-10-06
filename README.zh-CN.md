# Arova Chrome 下载

[English](README.md) | **简体中文**

[下载版本](https://github.com/spencer17x/arova-releases/releases) · [功能介绍](FEATURES.zh-CN.md) · [使用指南](USAGE.zh-CN.md)

本仓库分发 Arova Chrome 官方编译包、校验摘要和发布元数据，不包含应用源码或私有开发历史。

Arova 提供公开 GigaX 信号发现及私人地址钱包监控。独立网站和 Chrome 插件共享账号数据；插件在支持的 XXYY、GMGN 和 DeBot 页面展示通知，账号、钱包与通知配置在管理页完成。监控节点由平台维护，账号默认赠送 100 个启用地址额度，多链同地址计一次，暂停释放名额。

当前客户端已用钱包地址配置替代旧 Fomo/Pump 连接流程，不要求提交 Fomo/Pump 会话或私钥。旧平台动态、Pump Top、Arova 聪明钱包/钱包共振信号已退役。

## 安装与更新

1. 在 Releases 下载 `arova-chrome-VERSION.zip`，解压到长期保留的目录。
2. 打开 `chrome://extensions`，开启“开发者模式”。
3. 首次安装点击“加载已解压的扩展程序”，选择直接包含 `manifest.json` 的目录。
4. 更新时替换原目录内容，点击“重新加载”，再刷新交易页面。保留原插件安装可保留浏览器设置。
5. 点击 Arova 工具栏图标，登录并添加钱包地址、通知目标。

GitHub ZIP 不会自动更新。应安装插件 ZIP，而不是 GitHub 自动生成的 Source code 源码包。Beta 仍为预发布，请使用具体版本页面，不依赖 Latest 快捷入口。

## 发布文件

- `arova-chrome-VERSION.zip`：包含商业许可及第三方声明的插件包。
- `SHA256SUMS`：插件包校验摘要。
- `release-info.json`：版本、构建提交、生产 API、插件 ID 和摘要。

固定插件 ID：`gedflalfmklfccgaabdbcnjjchlfemfo`。生产 API：`https://api.arova.top`。

公开 tag 是独立分发快照。自动生成的 Source code 压缩包仅包含公开文档及分发产物，不包含私有应用仓库；插件运行所需的编译后 JavaScript 包含在插件 ZIP 内。

## 范围与许可

Arova 提供监控和提醒，不提供自动交易或保证收益。RPC 历史不足、未支持路由及跨链归属不明可能影响覆盖，详见[使用指南](USAGE.zh-CN.md)。

Arova 采用专有商业许可，见 [LICENSE](LICENSE)；第三方声明保留于 `THIRD_PARTY_NOTICES.txt`。公开下载不代表应用开源，方案和账号权益由服务端管理。

会员筹备：Free 10 钱包，Plus 100（$29/月或 $290/年），Pro 300（$79/月或 $790/年）。付款及新账号体验规则仍关闭，原赠送保留。按自然月/年、手动续费；同账期升级补差，降级下期生效，年付转发额度按月重置。网站和插件可查看当前会员状态。

GigaX 卡片与通知不再显示价格行，保留市值、涨幅、合约和供应商原文。
