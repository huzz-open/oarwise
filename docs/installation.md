# Oarwise 行舟安装说明 / Installation

固定下载入口：[官网个人信息页](https://oarwise.com/account)。官网自动提供当前安装包，店铺入口与本指南不随发行版本改变。

## 1. 把安装压缩包交给 Agent

从官网下载的 `*-encrypted.zip` 是加密外层。使用 7-Zip 和账号邮箱收到的对应版本密码解压一次，得到以下无需密码的安装压缩包之一：

| 客户端 | 交给 Agent 的文件 | 本说明在包内的位置 |
|---|---|---|
| Codex | `computer-use-ext-codex.zip` | `computer-use-ext/INSTALL.md` |
| DSH | `computer-use-ext-dsh.tgz` | `package/INSTALL.md` |
| 兼容 Agent / Skill | `computer-use-ext-skill.zip` | `computer-use-ext/INSTALL.md` |

把这个内层 ZIP 或 TGZ 拖入对应 Agent 的对话，并说：

> 请读取压缩包内的 INSTALL.md，帮我安装行舟。保留完整运行文件，并按说明检查宿主支持和安装结果。

无需再次手工解压或重新压缩。Agent 必须能读取本地附件并安装本地插件；仅支持云端聊天的界面无法在你的电脑上安装。如果不接受压缩包附件，将压缩包保存在本机，把绝对路径交给有本地文件能力的 Agent。解压密码只用于本地解开外层，不必发给 Agent。

## 2. 安装执行说明

1. 仅支持 Windows。按收到的包选择下面对应方式，完整保留 runtime、资源及隐藏目录，不单独移动 EXE。不要覆盖其他插件或无关配置。
2. **Codex**：将内层 ZIP 完整解压到持久的本地目录，根目录应有 `.agents/plugins/marketplace.json` 和 `computer-use-ext`。执行 `codex plugin marketplace add <该根目录的绝对路径>`，再执行 `codex plugin add computer-use-ext@oarwise-local`；含空格的路径须加引号。运行插件的 `setup-codex-hooks` 设置技能，由用户在 Hooks 设置中审查并信任 Stop／Interrupt，之后用新本地对话检查工具连接。安装不等于用户已信任 hooks，不写入或绕过信任配置。
3. **DSH**：把内层 TGZ 交给 DSH 插件管理器安装，保留其 npm 归档结构。确认 `@oarwise/dsh-computer-use-ext` 已启用，并检查工具和 Skill 可用；无需再单独登记 MCP 或复制 Skill。
4. **Skill**：解开内层 ZIP，将整个 `computer-use-ext` 目录放入宿主的 skills 目录，按 `SKILL.md` 和 `host/README.md` 接入。宿主必须支持本地持久进程、工具调用，以及结束／取消时的进程和窗口资源清理；不满足时应说明缺失能力。普通聊天提示词不具备这些能力。
5. 按插件 `account_login` 返回的官网入口，由用户在网站完成账号验证和设备连接，再用 `account_status` 检查。不得索取或将注册码、邮箱验证码、解压密码写入聊天或日志。安装、授权、宿主清理配置分别确认；只有用户授权具体窗口任务后才操作窗口。

## 3. English instructions

Extract the downloaded `*-encrypted.zip` once with 7-Zip and the version-specific password from your account email. The result is a password-free installer archive: `computer-use-ext-codex.zip`, `computer-use-ext-dsh.tgz`, or `computer-use-ext-skill.zip`. Drop that inner archive into a compatible local Agent and ask it to read the included `INSTALL.md` and install Oarwise. No manual recompression is needed. If attachments are unsupported, provide its absolute local path to an Agent with local file access. Keep the extraction password out of chat.

1. Windows only. Keep the complete runtime and resources. Preserve unrelated user configuration.
2. **Codex**: fully extract the inner ZIP into a persistent directory containing `.agents/plugins/marketplace.json` and `computer-use-ext`. Run `codex plugin marketplace add <absolute-root-directory>` followed by `codex plugin add computer-use-ext@oarwise-local`. Quote paths containing spaces. Run the bundled `setup-codex-hooks` skill; the user must review and trust Stop/Interrupt in Hooks settings. Verify tool connectivity in a new local chat. Do not bypass hook trust.
3. **DSH**: install the inner TGZ through Plugin Manager and confirm `@oarwise/dsh-computer-use-ext` is enabled with its tools and Skill. Do not separately register MCP or duplicate the Skill.
4. **Skill**: extract the inner ZIP and copy the complete `computer-use-ext` directory into the host's skills directory. Follow `SKILL.md` and `host/README.md`. The host must own persistent local processes and clean up on completion/cancellation; report missing capabilities rather than assuming ordinary chat supports them.
5. Let the user complete account and device connection on the website returned by `account_login`, then check `account_status`. Never request credentials or extraction passwords in chat or logs. Verify installation, authorization and host cleanup configuration separately; operate windows only for a user-authorized task.
