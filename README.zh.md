# Polymath for Windows

[English](README.en.md) | [Русский](README.ru.md) | [Українська](README.uk.md) | [Deutsch](README.de.md) | [Español](README.es.md) | [Français](README.fr.md) | [Polski](README.pl.md) | [Türkçe](README.tr.md) | [中文](README.zh.md)

**Your quiet AI partner, in every conversation**
（你在每一场对话中的安静 AI 伙伴）

Polymath 坐在你身边，在你词穷或缺乏知识时帮你。它能听到对方说的话，看到你屏幕上的内容，并建议你下一步该怎么做。别人看不到它，它也从不替你说话。

### 为什么需要它

- **与你不懂其语言的人交流。** Polymath 会听对方说话并显示对方说了什么，然后建议你用对方的语言和你的母语怎么回答（这样你始终清楚自己对对方说了什么）。你自己留在对话中，而不是躲在翻译后面。
- **在线交友。** Polymath 可以关注你的屏幕，并建议你用对方的语言和你的母语如何回复（这样你始终清楚自己写了什么）。你写出的消息听起来就是你，只是更好。
- **调情。** 在你需要的那一刻，获得回复的想法、一个笑话或一句赞美。
- **日常事务。** 提出问题，用应用截取屏幕截图，获得适合你具体情况的回答。
- **复杂又看不懂的事。** 不知道该点哪里，或者不知道为什么某样东西不工作？把屏幕给 Polymath 看，它会指出错误，并告诉你如何改正。

### 曾经让人害怕的事，有了 Polymath 就能做到

- 参加在线面试，并知道该说什么。
- 设置 Google 或 Meta 广告，不浪费预算。
- 做出你的第一个网站，并放到任何主机上。
- 看懂租赁或贷款合同，不漏掉小字条款。
- 填写纳税申报表或办理签证，文件不出错。
- 写出能脱颖而出的简历和求职信，包括用外语写。
- 谈价格或折扣，与房东、承包商或客户商量条件。
- 看懂银行、税务局或保险公司的来信，弄清他们真正想要什么。
- 在什么都不工作、而技术人员太贵或联系不上时，设置 Wi-Fi 路由器、打印机或手机。
- 给商店、航空公司或物业公司写一封有说服力的投诉信。
- 为与老板、伴侣或父母的艰难谈话做好准备，找到合适的话。

以前这需要身边有专家，或者给朋友打电话。现在你有 Polymath，它精通各个领域，随时在你身边。

---

一个用于对话和会议的小型辅助工具栏。它能听对方说话并把声音翻译成您的语言，用对话所用的语言建议回答，解决屏幕上的任务，并在聊天中回答任何问题。

**只有您能看到这个工具栏。** 在 Zoom、Teams、Meet、Discord 和 OBS 中共享屏幕时，它不会出现，在截图和录屏中也不会出现。

## 功能

- **Listen** (`7` / `Ctrl` + `Alt` + `7`)。监听电脑的声音（通话中对方的声音），识别语句，显示翻译成您母语的内容，当对方对您说话时，还会给出用对话语言写好的回答及其翻译。点击回答即可复制。“仅在需要回答时”模式只显示需要您回答的语句。
- **Screenshot** (`2` / `Ctrl` + `Alt` + `2`)。把屏幕截图发给模型：解题、回答测验问题、审查代码。
- **Watch** (`4` / `Ctrl` + `Alt` + `4`)。监视屏幕，当屏幕上出现新的问题或任务时给出回答。10 分钟后自动关闭。
- **聊天**。普通提问。开头的数字用来选择命令：`1` Quick（简短，快速模型），`3` Answer（针对最后听到的问题给出一个回答，并考虑对话内容），`5` Translate。
- 模型能看到对话的最后几句话，所以在聊天中您可以问“我该如何回答他们最后的问题？”。
- **知识库**。您自己的 `.txt` 和 `.md` 文件，里面有常见问题的现成答案。合适的答案在电脑上查找，无需联网，在模型还在回答时就立即显示。

## 安装

成品文件位于 `dist` 文件夹：

- `Polymath-Setup-<版本>.exe` - 安装程序，跟随 Windows 语言，支持 22 种语言：可以选择文件夹，无需管理员权限，会在桌面和开始菜单创建快捷方式，安装后程序自动启动；

Windows SmartScreen 可能会提示未知发布者（文件未签名）。点击“更多信息”，然后点击“仍要运行”。

系统要求：Windows 10 版本 2004（2020 年 5 月）或更高，Windows 11。在更旧的系统上，屏幕捕获隐藏功能无法工作。

## 首次启动

1. 打开设置（工具栏上的齿轮）。
2. 选择模型提供商，粘贴 API 密钥，然后点击“保存密钥”。“获取密钥”链接会打开提供商的页面。
3. 点击“测试连接”。会出现可用模型列表，点击某个模型即可填入字段。
4. 指定您的母语。在“知识库”部分的“关于您”中简要介绍自己（工作、经验）。模型会在回答中使用这些信息。
5. 点击“保存”（或 Ctrl+S）。

### 提供商

| 提供商                       | 默认模型                 | 图像 (Screenshot/Watch)     | 直接处理声音   |
| ---------------------------- | ------------------------ | ----------------------- | -------------- |
| Google Gemini                | gemini-flash-lite-latest | 是                      | 是             |
| OpenAI                       | gpt-5-mini               | 是                      | 否             |
| Anthropic Claude             | claude-sonnet-5-5        | 是                      | 否             |
| OpenRouter                   | openrouter/auto          | 是                      | 否             |
| Groq                         | openai/gpt-oss-120b      | 否                      | 否             |
| Mistral                      | mistral-medium-latest    | 是                      | 否             |
| Ollama（本地）               | llama3.2                 | 否                      | 否             |
| 自定义（兼容 OpenAI）        | 任意                     | 取决于模型              | 否             |

提供商会更改模型名称。如果找不到某个模型，请点击“测试连接”并从列表中选择一个。

“快速模型”用于 Quick 和 Translate 命令。可以留空，此时使用主模型。

当某个模型返回 503（过载）或 429（无额度）时，程序会立即询问这一对中的另一个模型。

### 备用模型

设置中的“备用模型”部分：当上面两个模型都返回 503 或 429 时，程序会询问的另一个提供商。例如 Anthropic Claude（默认 `claude-haiku-5-5`，速度快）。备用密钥单独保存。没有备用密钥时，使用“模型”部分中同一提供商的密钥。如果备用模型无法读取所发送的内容，则会被跳过：屏幕图像（Screenshot/Watch）或声音。

## 语音识别（用于 Listen）

设置中的“语音识别”提供四种引擎：

1. **通过模型**（默认）。语句直接发送给聊天模型。使用同一个密钥即可配合 Google Gemini 工作。
2. **云端 Whisper API**。OpenAI（`whisper-1`、`gpt-4o-mini-transcribe`）、Groq（`whisper-large-v3-turbo`，快速且便宜）或您自己的兼容 OpenAI 的服务器。识别密钥与模型密钥分开保存。
3. **本地 (whisper.cpp)**。声音永远不会离开电脑。用一条命令安装：

```powershell
powershell -ExecutionPolicy Bypass -File scripts\install-whisper.ps1
```

在已安装的程序中，脚本位于 `<程序文件夹>\resources\scripts`。选项：`-Model tiny|base|small|medium|large-v3-turbo`（默认 small，466 MB）以及用于 NVIDIA 显卡的 `-Cuda`。文件保存到 `%APPDATA%\Polymath\whisper`。然后选择“本地”，点击“测试识别”。

4. **本地 (NVIDIA Parakeet)**。同样在本机运行，在处理器上比 whisper.cpp 更快，通常也更准确。模型 `parakeet-tdt-0.6b-v3` 支持 25 种欧洲语言（英语、俄语、乌克兰语、德语、法语、西班牙语等），但不支持土耳其语和中文。通过 [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) 运行。设置中的“下载 Parakeet”按钮会把一切就位，或者用一条命令：

```powershell
powershell -ExecutionPolicy Bypass -File scripts\install-parakeet.ps1
```

总共约 520 MB。选项 `-Model v2` 会获取仅支持英语的模型，英语略更准确。文件保存到 `%APPDATA%\Polymath\parakeet`。然后选择“本地 (NVIDIA Parakeet)”，点击“测试识别”。停顿后的第一句话需要等待 7-10 秒加载模型，之后的语句用时不到一秒。10 分钟没有语音后，服务会停止并释放内存。 两个下载（程序和模型）都会根据 GitHub 公布的 SHA-256 校验。不匹配的文件会被丢弃，不会安装任何内容。没有公布的哈希就不会安装。

在新电脑上首次启动时，工具栏会询问一次如何识别语音：通过 Gemini（无需下载），或在本机使用 Parakeet（应用会下载约 520 MB，带进度和取消按钮）。之后可以在设置中更改这个选择。

“测试识别”按钮对四种引擎都有效。

## 使用方法

| 操作                               | 快捷键                         |
| ---------------------------------- | ------------------------------ |
| 显示 / 隐藏工具栏                  | `Ctrl` + `Alt` + `P`           |
| 快速回答（简短，快速模型） | `Ctrl` + `Alt` + `1` |
| 解决屏幕上的任务                   | `Ctrl` + `Alt` + `2`           |
| 回答刚听到的问题 | `Ctrl` + `Alt` + `3` |
| 监视屏幕（开/关）                  | `Ctrl` + `Alt` + `4`           |
| 翻译 | `Ctrl` + `Alt` + `5` |
| 监听通话（开/关）                  | `Ctrl` + `Alt` + `7`           |
| 点击穿透工具栏（开/关）            | `Ctrl` + `Alt` + `T`           |
| 发送                               | `Enter`                        |
| 换行                               | `Shift` + `Enter`              |
| 停止回答                           | `Ctrl` + `.` 或 `■` 按钮       |
| 新对话                             | `Ctrl` + `N` 或 `+` 按钮       |
| 上一条请求                         | 在空字段中按 `↑` / `↓`         |
| 隐藏工具栏                         | `Esc`                          |

### 短命令和长命令

短命令在工具栏内使用，长命令（带 `Ctrl` + `Alt`）可在任何窗口使用。在空输入框中输入数字即可选择命令，`1 您的文字` 也可以。

| 操作 | 短（在工具栏中） | 长（在任何窗口中） |
| --- | --- | --- |
| 快速回答（简短，快速模型） | `1` | `Ctrl` + `Alt` + `1` |
| 解决屏幕上的任务 | `2` | `Ctrl` + `Alt` + `2` |
| 回答刚听到的问题 | `3` | `Ctrl` + `Alt` + `3` |
| 观察屏幕（开/关） | `4` | `Ctrl` + `Alt` + `4` |
| 翻译 | `5` | `Ctrl` + `Alt` + `5` |
| 监听通话（开/关） | `7` | `Ctrl` + `Alt` + `7` |
| 显示 / 隐藏工具栏 | `Esc` | `Ctrl` + `Alt` + `P` |
| 点击穿透工具栏（开/关） | - | `Ctrl` + `Alt` + `T` |
| 设置 | `Ctrl` + `,` | `Ctrl` + `,` |
| 新对话 | `Ctrl` + `N` | - |
| 停止回答 | `Ctrl` + `.` | - |
| 显示所有快捷键 | `F1` | - |

**工具栏被隐藏了？** 按 `Ctrl` + `Alt` + `P`（或设置中指定的快捷键），或再次启动 Polymath（开始菜单快捷方式），工具栏就会恢复。托盘图标默认关闭。工具栏中的 `?` 按钮（在设置旁边，或 `F1`）会显示所有命令和快捷键。

**重要：** 短命令仅在输入框处于活动状态时有效，在点击穿透模式下无效。长命令（带 `Ctrl` + `Alt`）始终有效。

快捷键可在设置中更改：点击输入框并按下组合键。如果其他程序已占用，工具栏会提示。

拖动标题即可移动工具栏，位置会被记住。宽度、不透明度和字号都可以调整。

### 外观和鼠标

设置中的“界面”部分：

- **主题** - 深色（石墨，默认）或浅色（象牙）；
- **工具栏不透明度** - 整个工具栏连同文字（30-100%）；
- **背景不透明度** - 仅工具栏背景，文字保持清晰（20-100%）；
- **点击穿透工具栏** - 点击会穿过辅助工具栏，到达下面的窗口。工具栏无法用鼠标移动或点击，键盘和快捷键仍然有效。用 `Ctrl` + `Alt` + `T` 切换，此时工具栏标题会显示“点击穿透”标记。设置窗口始终是普通窗口；
- **悬停即可按下按钮** - 把光标停在工具栏的按钮上（默认 3 秒，可设 1.5 到 5 秒），按钮会自动按下。按钮下方会有一条进度条逐渐填满。在点击穿透模式下也有效。

Listen 捕获整个系统的声音。请使用耳机：这样只会录到对方的声音，而不是您自己的声音。

## 您自己的命令

数字命令位于 `%APPDATA%\Polymath\commands.json`（设置中的“打开 commands.json”按钮）。每次调用都会重新读取该文件，无需重启。示例：

```json
{
  "1": {
    "name": "Interview",
    "instructions": "Answer as a senior Java developer at a job interview. Answer in {conversation_language}, then give a short translation into {native}.",
    "model": "main"
  }
}
```

字段：`name`、`instructions`（必填），`model`（`main` 或 `small`），`screen: true`（附加屏幕截图），`watch: true`（监视屏幕），`listen: true`（开启 Listen）。占位符：`{native}` - 您的语言，`{conversation_language}` - 对话语言。

## 隐藏有多可靠

窗口使用 `SetWindowDisplayAffinity(WDA_EXCLUDEFROMCAPTURE)` 创建。这是 Windows 的机制：截图会在该位置显示窗口下面的内容。Zoom、Teams、浏览器中的 Google Meet、Discord、OBS、截图工具、PrintScreen 和 Xbox Game Bar 都遵守这一机制。

此外：

- 任务栏上没有按钮，Alt+Tab 中没有条目；
- 托盘图标默认关闭（共享整个屏幕时可以看到托盘）；
- 没有系统弹出窗口：提示、列表和菜单都绘制在工具栏内部，上下文菜单已禁用。

局限：

- 隐藏功能无法防范对准显示器的摄像头，也无法防范硬件 HDMI 捕获。
- 如果您共享的是某个程序的**窗口**（而不是整个屏幕），并且工具栏位于其上方，对方会看到工具栏下面的内容。这是预期行为。
- 早于 Windows 10 版本 2004 的系统会在捕获中显示黑色矩形来代替工具栏。
- 打开的链接和文件（commands.json、数据文件夹）会在普通程序中打开，共享屏幕时可以被看到。

在您自己的电脑上检查隐藏效果：

```powershell
powershell -ExecutionPolicy Bypass -File scripts\verify-capture.ps1
```

脚本会显示两个受保护的测试窗口和一个普通窗口，用两种方式捕获屏幕并输出结果。出现 `RESULT: Polymath windows are hidden from screen capture` 这一行，说明一切正常。

## 知识库

设置中的“知识库”部分：

- **关于您** - 关于您的一般信息。模型在每个回答中都会使用。
- **文件** - 点击“添加文件”按钮，或把 `.txt` 和 `.md` 文件拖到该部分。文件会被复制到 `%APPDATA%\Polymath\knowledge`（“打开文件夹”按钮）。您可以在那里编辑，程序会自动获取更改。同名文件会被替换，最大 2 MB，编码为 UTF-8、UTF-16 或 Windows-1251。
- **在回答中使用知识库** - 知识库中有文件时即可开启。
- **在模型回答之前，立即显示知识库中的匹配项** - 同样如此。

工作原理。对于聊天中的问题，以及 Listen 中对方的每一句话，程序会先在您的文件中查找答案，无需联网，也无需模型。匹配项会立即以蓝色的“来自知识库”区块显示在模型回答之上，旁边有“复制”按钮。同时，模型会收到这些数据（知识库较小时是全部内容，否则是匹配的部分），并据此作答。搜索能理解词的不同形式。本地搜索找不到其他语言的问题，但模型仍会根据知识库作答。

文件的三种写法任选其一：

```markdown
# What salary do you expect?
From 5,000 USD net, open to discussion.

# Why are you leaving your current job?
I want more architecture work.
```

```text
Q: What is your notice period?
A: Two weeks.
```

或者只是用空行分隔的段落：段落的第一行较短的话，就是它的主题。

## 历史记录和导出

设置中的“历史记录”部分：

- **将历史记录保存到磁盘**。默认关闭：此时历史记录只存在于内存中，直到程序关闭。开启后：每个问题和回答都会追加到 `%APPDATA%\Polymath\history\YYYY-MM-DD.jsonl`，每一行都用 Windows DPAPI 加密（只有您的 Windows 账户能读取）。
- **历史记录中的名字**。在导出内容中为您的提问署名。留空表示使用 Windows 用户名。
- **保留天数**。启动时会删除更早的日期。0 表示全部保留。
- **导出**本次会话、今天、7 天、30 天或全部时间。“导出为 .txt”会把文件保存到 `Documents\Polymath`，“复制为文本”会把同样的文本放入剪贴板。
- **清除历史记录**会删除历史文件和本次会话的记录（按两次按钮）。

记录的内容：

- 聊天：Q - 您的问题（带命令和屏幕截图标记），A - 模型的回答；
- Listen：Q - 对方的语句及其翻译，A - 建议给您的回答及其翻译（需要回答时）；
- Watch：对屏幕上任务的回答，空运行不会被记录。

导出文件未加密。通过“显示文件”按钮打开的资源管理器和记事本，在共享屏幕时可以被看到。

## 隐私

- API 密钥由 Windows 加密保存（通过 Electron safeStorage 使用 DPAPI），位于 `%APPDATA%\Polymath\settings.json`。
- 默认情况下历史记录只在内存中，程序关闭后消失。保存到磁盘需要在设置中开启，历史文件用 DPAPI 加密。
- 知识库文件以未加密形式保存在 `%APPDATA%\Polymath\knowledge`，搜索在电脑上进行。它们只会随提问发送给模型：知识库较小时是全部内容，否则是匹配的部分。
- 声音和屏幕截图只会发送给所选的提供商（或备用提供商），并且仅在 Listen、Screenshot 或 Watch 开启期间。使用本地 whisper.cpp 或 Parakeet 时，声音永远不会离开电脑。
- 错误日志：`%APPDATA%\Polymath\logs\app.log`（不含对话文本）。

## 后台运行

“登录 Windows 时启动（隐藏）”复选框会让 Polymath 隐藏启动。用 Ctrl+Alt+P 呼出工具栏。手动方式：`Polymath.exe --background`。

## 更新

已安装的 Polymath（来自 `Polymath-Setup`）会在启动几秒后检查新版本。未经您同意不会下载任何内容：面板上会显示“Polymath X 已发布”，带有“更新”和“稍后”按钮，下载完成后显示“重启并更新”。Polymath 会关闭、覆盖安装旧版本并重新启动，设置、密钥和历史记录都会保留。如果开启了托盘图标，其菜单中有“Check for updates”。从源码文件夹运行的副本和便携副本不会自动更新。

下载的文件会根据发布版 `latest.yml` 中的 SHA-512 校验。没有该哈希的发布版会被拒绝，不匹配的文件不会安装。每次构建都会检查 `latest.yml` 中是否有正确的哈希。安装程序尚未做代码签名，因此 Windows SmartScreen 仍可能提示警告。

## 面向开发者

需要 Node.js 20 或更高版本。

```powershell
npm install
```

```powershell
npm start
```

```powershell
npm test
```

```powershell
npm run dist
```

- `npm test` - 单元测试（语句检测器、WAV、回答解析、SSE、命令、设置、模型客户端、历史记录）。
- `npm run dist` - 在 `dist` 中生成安装程序，然后检查 `latest.yml` 中是否有正确的 SHA-512。
- `python scripts/make-installer-art.py` - 根据 `assets/icon.png` 重新绘制安装程序的图片（`build/`：侧边图、页眉、图标）。需要安装了 Pillow 的 Python。
- `npm run capture-test` - 内置的隐藏检查（结果为 JSON）。
- 环境变量 `POLYMATH_VISIBLE=1` 在开发模式下关闭隐藏，用于截取界面截图。对已构建的程序没有任何作用。

结构：

- `src/main` - 主进程：窗口、快捷键、模型、语音识别、Listen、Watch；
- `src/renderer` - 工具栏和设置窗口，系统声音捕获；
- `src/shared` - 共享代码：语句检测器、WAV、文本解析、SSE、界面翻译；
- `scripts` - whisper.cpp 和 Parakeet 的安装以及隐藏检查；
- `tests` - 测试。
