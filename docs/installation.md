# 安装指南

## 1. 下载与解压

访问 [个人信息页](https://oarwise.com/account)，完成邮箱验证和注册码兑换。权益有效时可下载 Codex 或 DSH 的加密 ZIP。

安装包解压密码发送到账号邮箱。未收到时，可在个人信息页选择“重发解压密码”。使用 [7-Zip](https://www.7-zip.org/) 打开 ZIP 并输入邮件中的对应版本密码。

## 2. Codex

完整解压 Codex ZIP，保留 `.agents` 和 `computer-use-ext` 两个目录。将实际解压目录作为本地插件市场添加。

```bash
codex plugin marketplace add <解压目录>
codex plugin add computer-use-ext@oarwise-local
```

如果已有旧版同名本地市场，先从 Codex 插件管理中移除旧市场，再添加新版解压目录。安装完成后打开新聊天使用。按照插件提供的 setup-codex-hooks 指引审查并启用会话结束和中断清理。

## 3. DSH

解压 DSH ZIP 后得到 `computer-use-ext-dsh.tgz`。在 DSH 插件管理器中选择本地安装包，安装并启用 Computer Use Ext。安装完成后打开新会话，按提示登录并连接电脑。

## 4. 连接电脑

插件给出设备确认链接后，在官网登录原邮箱，确认连接该设备。返回客户端检查账号状态，成功授权后即可使用。

## 5. 验证

可以让 AI 查找一个已有窗口并后台截图。核对截图内容后，再按实际任务进行点击或输入。完成任务后关闭会话释放窗口资源。版本可在客户端插件列表查看。
