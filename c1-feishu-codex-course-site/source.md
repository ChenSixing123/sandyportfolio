<title>C1 基础办公：Codex + 飞书 协同办公</title>

**前言**

**2026 年 4 月 16 日**，我的校外导师 Marc 在公司内做了一次分享，主题是他最近一个多月探索的 **WorkBuddy + Obsidian 知识管理模式**。听完之后，我当时很好奇地问了他一个问题：为什么不用飞书，而要重新选择 Obsidian？

他给我的一个回答让我印象很深：**飞书里的内容，不太方便被 AI Agent 读取和修改。**

**2026 年 3 月 28 日，飞书 CLI 的开源引起热议。**

<grid>
<column width-ratio="0.458470">
![图片展示了数字生命卡兹克在AI](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=NzEyNzg5MTM4YmZjYjk1ZTkyMmNhMzU2MGMxM2M0ZjlfY2QxZmVlNWViZDVhYTIwMmI1ZjdlMzdmODFjMjc5OTVfSUQ6NzY0NjY4NDQwNzcwOTM3MTM2NF8xNzgyODI0MDAxOjE3ODI4Mjc2MDFfVjM)
</column>
<column width-ratio="0.541530">
![图片展示了飞书CLI相关的多个内容。上方左侧是“把Claude Code接入飞书”的教程及演示，中间是“飞书CLI实战全程干货”，右侧是“不仅记录待办还能把待办直接办了”。下方左侧是“AI接管飞书后，我快下班”的内容，中间是“OpenAI实时语音+飞书CLI，实现口述式写文档”，右侧是“飞书，有了全新的使用方式”。这些内容与上下文提到的2026年3月28日飞书CLI开源引起热议相呼应，展示了飞书CLI在飞书中的应用及相关讨论。](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=OTU1YmIyMWQ0NDA4NDU1NjFjNjQ2OTY3YmQ0ZmI2NDBfZDY5MmQyOGJlOTNjZDk1ZTY1MTFiZThkNTJmZjViMjFfSUQ6NzY0NjY4NDQ4MTQxNjI4NTM3OF8xNzgyODI0MDAxOjE3ODI4Mjc2MDFfVjM)
</column>
</grid>

在过去的非 AI 时代，飞书已经是非常优秀的企业协作工具。它解决的是**人与人之间**的信息流转：大家可以在飞书里聊天、开会、写文档、做表格、推进项目。它的核心价值，是让组织内部的人可以更高效地协同办公。

但到了 **AI Agent 时代，协作关系正在发生变化**。企业内部的协作对象不再只有“人”，还会逐渐加入各种 AI Agent，比如 Codex、Claude Code、WorkBuddy 等。

这时候，一个新的问题就出现了：**如果 AI Agent 不能方便地读取飞书里的文档、表格、会议纪要和项目资料，也不能安全、稳定地修改这些内容，那么飞书就很难真正成为 AI 办公时代的工作入口。**

飞书需要解决**人与 AI Agent** 之间的交互。飞书 CLI 它背后的意义，不只是多了一个开发者工具，而是飞书开始补齐面向 AI Agent 的基础设施。

**AI Agent + 飞书 这是一个巨大的AI应用场景。**



# 飞书CLI是什么？

**飞书新推出的命令行工具（CLI），让AI Agent能直接操作飞书，实现自动化办公**。简单来说，就是**给AI一个“遥控器”，让它帮你发消息、查日程、写文档、整理会议纪要等**。

# 展示案例

## ✅ 读取现有飞书文档，进行内容的增添删改

<grid>
<column width-ratio="0.457798">
![图片展示的是飞书聊天窗口中的对话内容。对话中提及可以读取飞书链接，解析出的是一个飞书Wiki文档，给出了文档标题、类型、Wiki node_token、文档obj_token及所有者等信息。还表示已成功读取正文内容，并列举了文档大概目录。此外，提到后续可基于该文档提供总结、改写等帮助。该图片与上文“Codex可以直接读我的飞书文档，并且帮我修改内容”的描述相呼应，直观呈现了Codex读取飞书文档的实际对话场景。](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=OWRhODUzYzU2MjE0Mjg5ODkyOTIyZTE2ZmU2MGNmZWVfMDRkNzdmNWQ2OGY2N2RjY2FkYjIxODgxNzFiMmQyNjFfSUQ6NzY0NjY4MTE2MjkwNTQyMzA0OV8xNzgyODI0MDAxOjE3ODI4Mjc2MDFfVjM)
</column>
<column width-ratio="0.542202">
![图片展示的是飞书与Codex联动办公的界面，界面中有文字对话内容及文件处理信息。对话内容显示用户要求在文档“概览”中补充前情叙述，优化内容，系统反馈已处理完成，更新了概览部分并完善了课程安排，还重新读取确认过后续内容。下方显示已编辑2个文件，分别为codex - course - overview.xml（新增11处，无删除）和codex - course - updated.xml（新增1处，无删除）。这与上文提到的读取现有飞书文档进行内容增添删改的案例相契合。](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=YzAwMTEwZTIzMzQwNTE2ZjJlZTNmMDhlMjhkMmRmYThfZjg4OWFhN2E4YzJkNWQyZjdjMjA2YWMyN2FjOTI2ODBfSUQ6NzY0NjY4MTE1OTY2MzE0Mzg5NF8xNzgyODI0MDAxOjE3ODI4Mjc2MDFfVjM)
</column>
</grid>

## ✅直接创建云文档内容

<grid>
<column width-ratio="0.499115">
![图片展示的是Codex与飞书联动办公的 addCriterion](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=Yjg5ZmY1MjA5MmJkNTVlZWExYjg3NmYzZTFlMDU1ZWRfOGJhZGM2NGJjYzRhNzMxYjVkNDYzZGFkOWJhZmRjODZfSUQ6NzY0NjY4MTE2Mjg0NDY4NzU4M18xNzgyODI0MDAxOjE3ODI4Mjc2MDFfVjM)
</column>
<column width-ratio="0.500885">
![图片展示的是Codex与飞书联动后生成的云文档内容。上方提问能否在飞书里写一个云文档，下方回复已新建好，用的是user身份，可直接打开编辑，并附上安装教程，包含Mac和Windows版本，还列出了卡点如npm权限、命令名、未配置Mac Keychain等。下方还展示了本地Markdown文件“feishu - codex - install - guide.md”，并有“已编辑”标识，显示+448 - 0的修改量。该图片与上下文介绍的Codex与飞书联动能力相呼应，呈现了联动后的具体操作及文档内容。](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=MzUxYmViZjgwZDY2MjEyMGViZTFlNDNmMDJjYTBiMmVfNTQxYjljMTM4YmYwN2U4NmFhZDdiZmM1ODEyMTQzZDZfSUQ6NzY0NjY4MTE2MTU0NDc5NzExMl8xNzgyODI0MDAxOjE3ODI4Mjc2MDFfVjM)
</column>
</grid>

## ✅ 每日定时发送AI新闻

<grid>
<column width-ratio="0.543607">
![图片展示了 addCriterion```json{ "image_id": "1"}```](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=ZmUxMjFkMzE0OGIwNGRhNDdjNmZkNGQ1MzAwN2UwMzBfNGE4OWQzZTVkNzI4MmQxZjJkMmI3MmVhMzExYzhiN2ZfSUQ6NzY0NjY4MTE2MzExNzE4NjI1MV8xNzgyODI0MDAxOjE3ODI4Mjc2MDFfVjM)
</column>
<column width-ratio="0.456393">
![图片展示的是Codex与飞书联动后发送的AI简报界面。上方显示“AI 晨间简报”，更新时间为北京时间6月2日下午，时间范围为最近24小时。内容涵盖多个AI模型发布/更新，如阶跃星辰Step 3.7 Flash发布、JetBrains推出Mellum2等，每条个发布/更新均有来源、摘要及链接。下方有“可以向自己发送文件或转发消息”的提示。该图片与文档中“每日定时发送AI新闻”内容相关，直观呈现了Codex每天定时发送的AI简报样式。](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=MmYwNmM3NGI2NGJiMjk2Nzk3M2RiMDQwY2ExZTRjMjNfZmRjOGIzOTc1YmEyZDJmOTAzY2FjNzQ4NmY2MmRhMzBfSUQ6NzY0NjY4MTE2MjAxODcyMDk0N18xNzgyODI0MDAxOjE3ODI4Mjc2MDFfVjM)
</column>
</grid>



## ✅ 飞书联动能力思维导图

**需要另外安装飞书官方新发布的1个skill，参考 小红书博主 @张咋啦 的视频**

![图片展示的是Codex与 larksuite/cli的GitHub仓库界面，其中有一个黄色突出显示的区域，内有文字“截图发给Codex：帮我安装github上这两个skill，并且用小白语言解释能做什么、怎么用：larksuite/cli fuxiaoi/lark-chart-skill”。该图片与上下文紧密相关，上下文提到需要另外安装飞书官方新发布的1个skill，参考小红书博主@张咋啦的视频，此图可能是用于说明安装技能的具体操作或示例。](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=OWIyMmYxZjg5ZGI2NDVjOTMyZjM0MWIxMWRmYTZjNDJfOGQ4N2MzZDQ4MmQ1ZWFmM2U3NTg5ZWNmMjgyNjkzMTVfSUQ6NzY0NjY4MTE2MDk5OTY2ODkyMV8xNzgyODI0MDAxOjE3ODI4Mjc2MDFfVjM)

**以下内容为codex直接生成并贴入：**

下面这张思维导图梳理了 Codex 与飞书联动后可以覆盖的主要办公场景、自动化能力和常见配置卡点。

```mermaid
mindmap
  root((Codex × 飞书联动办公))
    飞书文档 Docx
      创建云文档
      读取与总结文档
      追加或替换内容
      生成周报 纪要 课程大纲
      插入图片 附件 画板
    知识库 Wiki
      解析 Wiki 链接
      读取节点内容
      维护课程资料
      沉淀团队知识资产
    即时消息 IM
      给自己发送消息
      发送 Markdown 简报
      搜索群聊与 chat_id
      读取聊天记录
      群消息受权限与外部群限制
    表格与多维表格
      读取飞书表格
      清洗与统计数据
      新增或更新 Base 记录
      做业务分析和看板原型
    日历与会议
      查询日程
      创建会议
      整理会议纪要
      提炼待办事项
    云盘与素材
      搜索文件
      上传下载文件
      导出文档资源
      管理权限与评论
    画板与可视化
      流程图
      架构图
      思维导图
      泳道图
      里程碑和甘特图
    自动化
      每日 AI 简报
      定时飞书推送
      轮询消息触发
      事件订阅 Webhook
    常见卡点
      npm 全局安装权限
      lark-cli 命令名
      config init 初始化
      auth login 用户身份
      keychain downgrade
      scope 权限不足
      外部群发送限制
```

# 如何安装飞书CLI? （具体见<cite doc-id="KxERw8P5lim5cIkX6LUcg4a7nIe" file-type="wiki" title="Codex 联动飞书 CLI 安装教程" type="doc"></cite>）

安装和配置是关键，通常分为三步：

1. **安装工具：让你的AI Agent工具（如 codex）执行安装命令`npm install -g @larksuite/cli `（如果不行的话，可以在自己的终端上安装）**

![图片展示了Codex在执行安装命令`npm install -g @larksuite/cli`时遇到权限审批超时的问题。Codex尝试执行此命令两次，但因权限权限审批超时，导致安装未成功。图片还给出了在本机终端直接运行`npm install -g @larksuite/cli`的解决方法，并提示若希望继续代装，需回复“允许安装”，再发起带权限的安装请求。该图片与上下文紧密相关，是对安装过程中可能遇到问题的说明及解决建议。](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=YmIxYjkzZGYyM2JkNTc0NmUwNWNhMGQxZDhmNWJlZWJfZThmMjljYTBhYzdkOWEyYzA4YzRjNDFhOWZiYTUzNjdfSUQ6NzY0NjQyODE5MzQwNjQzODM0N18xNzgyODI0MDAxOjE3ODI4Mjc2MDFfVjM)

![图片展示的是在终端中执行CLI相关命令的界面。首先输入`sudo npm install -g @larksuite/cli`安装工具，接着输入`npm list -g @larksuite/cli`查看已安装的版本，最后执行`lark-cli doctor`进行健康检查，显示`config_file`检查失败，提示需在后台运行`lark-cli config init --new`获取验证URL并打开浏览器操作。该图片与上下文介绍的安装和配置CLI工具流程相关，直观呈现了操作步骤及结果。](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=NWMyODM5NTRkYWExNjdjNzM0NjRkYWYzZTBiMGZmMTVfNWMwMmYxMzEwN2U5MDYxOGQzN2Q4MzZjNjM5NTQxMDhfSUQ6NzY0NjQyNzg4NjExOTI5MTgzNF8xNzgyODI0MDAxOjE3ODI4Mjc2MDFfVjM)

1. 配置授权：安装后，AI会引导你执行 `lark-cli config init` 命令，这会生成一个二维码，用飞书App扫码即可完成授权。

<grid>
<column width-ratio="0.537493">
![图片展示的是在终端执行`lark-cli config init --new`命令后生成的二维码界面。背景为深色，中间是用于飞书扫码配置应用的二维码，上方有文字“使用飞书 / Lark 扫码配置应用：”。其与上下文的关系是，文档在介绍Codex联动飞书CLI的安装和配置步骤时，提到配置授权环节执行`lark-cli config init`命令会生成二维码，用飞书App扫码完成授权，若未成功连接可运行`lark-cli config init --new`，此图片即运行该命令后生成的二维码画面。](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=Mzg5NGQ1NmYzNmQzYWQ4ZTZiNDM1N2VhOWQ4MDdiODZfOWY4YzJlMjU1OGI3ZjhjMDg2MWIxM2RhMDZiYjZiNjNfSUQ6NzY0NjQyNzk2OTY5MDM1NjkzM18xNzgyODI0MDAxOjE3ODI4Mjc2MDFfVjM)
</column>
<column width-ratio="0.462507">
![图片展示的是Codex与飞书联动时的连接状态及操作指引。上方显示“已处理4s”，下方提示“检查结果：还没有连接飞书”，并列出“lark-cli doctor”显示的“CLI已安装成功：1.0.44”及“配置文件失败：not configured”等信息。还给出下一步运行的代码“lark-cli config --new”，并说明其会输出验证URL，需在浏览器打开完成飞书授权，授权后再次运行“lark-cli doctor”，若显示“ok: true”则表示连接成功。此图](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=NjRiZmJkMzlkMzhmMThmOTk4ZDg0YzIzYzg3YTZmNjlfZWQ2MmY1OGM0ZjU3MjU3N2RiMTg0ZjE0ZjBhZmU0YzNfSUQ6NzY0NjQyODY4MTAzMTgzMDcwOF8xNzgyODI0MDAxOjE3ODI4Mjc2MDFfVjM)
**飞书扫码授权之后，再问 Codex 是否成功连接**
如果没有，可以在终端运行这一行代码
`lark-cli config init --new`
</column>
</grid>

**连接成功之后，你可以问 Codex 它如何和飞书进行联动？**

![图片展示了Codex与飞书CLI的联动操作示例。Codex询问如何使用飞书CLI，其回复称可直接调用命令“lark-cli”，并列出多个相关命令，如lark-cli doctor、lark-cli auth等，还说明一般流程包括配置飞书开放平台鉴权、检查配置等步骤。此外，它还介绍了CLI可实现的功能，如读取、创建飞书文档，以及电子表格的读写、查询、更新等操作。该图片与上下文](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=OGZkZTBjYWFjYjc2NTFmMzA0ZmE1M2IxNTZhYWMwNDVfYTFiNDIzMzI3NGUyNTliMDNjMzA3ZTk0NGEzMmFlNGJfSUQ6NzY0NjQyODQ0ODU2NjgwNzc3Nl8xNzgyODI0MDAxOjE3ODI4Mjc2MDFfVjM)

# 如何使用？（具体见<cite doc-id="RQL4d6ySVopVLgxXwLBc0K5HnAg" file-type="docx" title="飞书如何与 Codex 联动办公" type="doc"></cite>）

**授权成功后，你就可以直接用自然语言指令让AI帮你操作飞书了，比如“帮我查看今天的日程”或“把这段会议录音整理成纪要”。**

## **⚠️ 让 Codex 以 user 身份创建**

<grid>
<column width-ratio="0.482412">
![图片展示了Codex与飞书联动办公时，使用自然语言指令让AI操作飞书后生成的云文档内容。文档中提到一篇用bot身份创建的文档，CLI提示当前用户权限自动授权被跳过，需在飞书里授权或运行“lark-cli auth login”。下方有“feishu-codex-office.md”文档及“已编辑feishu-codex-office.md”字样，还显示了“打开方式”和“撤销”按钮。该图片与上文介绍的使用自然语言指令让AI操作飞书后生成云文档的内容紧密相关。](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=OWVhYjE5N2YyZmMyN2I3Mjc1OWI4NmRjNzUxOGNhMDZfOGM2YjllNTZmNTc5ZDVmNDVhMjJjMDkyNDdmZWM4OWJfSUQ6NzY0NjQxODk3MjMzMzcwNjQ2Ml8xNzgyODI0MDAxOjE3ODI4Mjc2MDFfVjM)
</column>
<column width-ratio="0.517588">
![图片展示了Codex与飞书联动办公中，让Codex以user身份创建文档的对话内容。用户询问如何编辑Codex飞书CLI生成的文档，Codex回复已用user身份重新创建了一份文档，但旧文档是bot身份创建，不一定有编辑权限。接着说明当前飞书应用缺少full_access权限，最简单方式是用这份新的user文档，让Codex创建飞书文档时直接说“用我的user身份创建飞书文档”，Codex会加上--as user，用户可自行编辑。](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=NDc2NzlhNmE0ZmRjMGI4OTkwODY0ZjM4OTMzMDc3MDBfMjNjODlhMDJjZWY1OGI3YWUyYWQxOWE2MTM3NjQwNGJfSUQ6NzY0NjQyMTA0NTA5MTY4MzU0NV8xNzgyODI0MDAxOjE3ODI4Mjc2MDFfVjM)
</column>
</grid>
