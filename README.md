# Oarwise 行舟

Oarwise 行舟是一款适用于 Windows 的通用 AI 后台电脑操作插件，为 Codex、DSH 及兼容 Agent 提供指定窗口的截图、点击和输入能力。

[官网](https://oarwise.com) · [账号与下载](https://oarwise.com/account) · [安装指南](docs/installation.md) · [问题反馈](https://github.com/huzz-open/oarwise/issues/new/choose)

## 1. 可以做什么

在支持的 Windows 应用中，可后台截图、点击和输入，不抢占键盘鼠标，不主动把任务窗口切到前台；兼容窗口最小化后仍可继续操作，让你在其他窗口处理工作。

- 发现并绑定指定程序窗口。
- 获取完整或局部截图，导出图片供 AI 查看。
- 后台点击、输入文字、按键、滚动和拖拽。
- 按聊天会话管理资源，结束或取消时清理。

行舟提供后台操作能力，AI 模型与 Agent 负责理解任务、规划步骤和判断结果。需要搭配支持图像理解与工具调用的模型，实际流畅度也受任务复杂度和应用兼容性影响。

## 2. 安装与激活

1. 付款后保存注册码和订单号，在 oarwise.com 使用邮箱完成验证并兑换注册码。
2. 在个人信息页下载 Codex、DSH 或 Skill 加密 ZIP，解压密码会发送到权益账号邮箱，也可点击“重发解压密码”。
3. 使用 7-Zip 和邮件密码解开外层 ZIP，再将内层 ZIP（Codex／Skill）或 TGZ（DSH）拖给对应 Agent，按包内 INSTALL.md 安装。官网自动提供当前安装包，无需更换店铺下载入口。
4. 按插件提示在官网确认连接这台电脑，返回客户端检查授权状态，再指定目标窗口进行操作。

[详细安装步骤](docs/installation.md) · [账号和设备管理](docs/account.md)

## 3. 选择安装包

| 使用环境 | 安装包 |
|---|---|
| Codex | Codex 插件 ZIP，含本地插件市场 |
| DSH | DSH 加密 ZIP，解压后安装 TGZ |
| 兼容 Agent | Skill ZIP，需支持本地持久进程和取消处理 |

三个包分别使用，通常只需下载一个。每个包均带完整运行组件，不需要另装 Python。没有单独的 All 合集包。

[GitHub Releases](https://github.com/huzz-open/oarwise/releases) 提供加密发行包和 SHA-256 校验值。使用密码解压后仍需账号和设备授权。密码按发行版本维护，遗失时可在官网个人信息页重新发送到账号邮箱。

## 4. 文档和反馈

- [产品说明与使用条件](docs/product.md)
- [常见问题](docs/faq.md)
- [官网产品介绍](marketing/website.md)
- [16688 商品说明](marketing/16688.md)
- [报告问题或提出建议](https://github.com/huzz-open/oarwise/issues/new/choose)

适用于 Windows 桌面应用，不支持 macOS、Linux 或手机系统。具体应用的截图、输入和最小化能力需要实际验证。本商品不包含 AI 订阅、API 额度或其他软件账号。
