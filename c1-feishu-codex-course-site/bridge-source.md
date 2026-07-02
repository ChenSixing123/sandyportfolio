<title>把 Claude Code 和 Codex 接入飞书：Lark Coding Agent Bridge</title>

<callout emoji="🚅">
重大升级！现在除了 Claude Code，也**已经支持接入 Codex**！
已经接入 Claude Code 的用户可以通过重启升级：
npx -y lark-channel-bridge@latest start
</callout>

龙虾虽然好玩，但是严肃办公场景下还是coding agent最靠谱！做了个bridge，可以把本地的Claude Code和Codex桥接到飞书/Lark里，让Claude Code/Codex成为飞书里的一个bot，可以像跟同事交流一样无缝跟Claude Code/Codex协作！

# 接入方式

<callout emoji="📍">
Repo链接：https://github.com/zarazhangrui/lark-coding-agent-bridge
</callout>

在Terminal输入一行命令即可：

```Plain Text
npx -y lark-channel-bridge@latest start
```

详细使用指南请阅读 [Readme](https://github.com/zarazhangrui/feishu-claude-code-bridge/blob/main/README.zh.md)

配合Lark CLI使用效果更好，如果没有安装过Lark CLI，请在这里安装：https://github.com/larksuite/cli

# 能实现哪些效果

## 手机上可以无缝跟Claude Code/Codex聊天

工作不再绑定在工位，可以散步时跟Claude Code/Codex聊天，还可以语音输入\~

如果是Mac电脑，可以考虑搭配[Amphetamine](https://apps.apple.com/us/app/amphetamine/id937984704?mt=12)使用，让电脑合盖的情况下也实现always on、永不休眠

![图片展示的是飞书手机端界面，显示Napoleon（Zara's Claude...）的聊天窗口。上方显示时间为5:29，有消息、文档/资料、图片/视频等标签。聊天内容中，Napoleon提到Phase C（B跑通后）剩余30个template等信息，并询问关于design.md格式、比例等问题，还提到今天先开Phase A并给出真实test演讲场景。界面底部有语音、文字输入等输入方式，底部蓝色圆圈为自动识别中英功能。该图片直观呈现了手机上无缝跟Claude Code聊天的场景，与文档中介绍手机上可无缝聊天的内容相契合。](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=ZDhmMWFmOGRkZThkMzFkMTEyYzZiMDI0ZTBlMGUzZjVfZTYyOWNkNjFiMjA3M2Q4NWRiNGNjNTMxMzdmMDhhZGFfSUQ6NzY0MTgzNTUwNzQwNTM3NjczMl8xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM)



## 多 session 管理：一个会话 =  一个session，取代 terminal tabs

<table><colgroup><col/><col/></colgroup><tbody><tr><td><b>Before</b></td><td><b>After</b></td></tr><tr><td>多session管理，一堆terminal tabs，非常容易乱套、找不到之前的tab在哪里<img name="CleanShot 2026-04-21 at 16.30.09@2x.png" alt="图片展示的是飞书界面中Claude Code项目的终端窗口。窗口显示版本号v22.22.1，路径为~/Documents/Claude code projects/tab - out git: (main) ，并有“claude --dangerously - skip - permissions”命令。窗口底部有“Landing page chips will now show the friendly domain name”等文字。该图片与文档中“手机上可以无缝跟Claude Code/Codex聊天”部分内容相关，直观呈现了在手机上使用Claude Code时的终端操作界面情况。" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=NzFiOTg1YzZjN2VjOTM0YTNiZWMxZDI1ZTVlM2VkOGNfYzI2MGMyNzdkZGUyYWI3MDljNDYzMWM1YmNkNTE2OGRfSUQ6NzY0MTgzNTUwNzE1NjQ4NzM2OV8xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM" mime="image/png" scale="1.000000" src="B4lQbzUE6o7oprxp6RPcYRvSnLd"/></td><td><ul><li>直接在飞书里用会话管理<ul><li>一个群 = 一个project</li><li>一个thread = 一个session（对应话题群中一个话题，或者普通群中一个thread）</li></ul></li><li>发送“/new chat （+你希望聊的话题）”，Claude Code/Codex就可以自动帮你创建一个新的群聊，不需要手动拉群</li></ul><grid><column width-ratio="0.567150"><img name="CleanShot 2026-04-23 at 16.59.28@2x.png" alt="图片展示了飞书群聊界面，群名为“CC for Project 自动生成" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=OGE4ZWRkZjk5NDllYmI0ZGVlNDgxMGEzMzYzNmNkOGVfYjg5NDA2OTc0Y2NiYjU2MmZlOWMyODcwNmUwZjA4MzFfSUQ6NzY0MTgzNTUwODU4NjQxNzExM18xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM" mime="image/png" scale="1.096096" src="Bh2DbSxE9op3SHx9GUXcknLunwd"/></column><column width-ratio="0.432850"><img name="CleanShot 2026-04-23 at 16.59.14@2x.png" alt="图片展示了飞书中的一个群聊 addCriterion，群名为“CC for Project A”，由1个人和1个机器人组成，机器人是Claude。该图片对应文档中“多session管理：一个会话=一个session，取代terminal tabs”部分内容，直观呈现了在飞书里用会话管理多session的场景，即一个群聊对应一个session，可自动创建群聊，方便管理。" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=MzcyZjYwMDA4NmJhYjY0MzBhMGNjNGQ3YmU2MjZjMTNfYmE2MzZmMzBmMDQ0YmI5OGM1ODg4MTkxMTYxOGE5NjlfSUQ6NzY0MTgzNTUwOTI2NTk5MjY1Nl8xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM" mime="image/png" scale="1.367041" src="KBuLbgTXlorQd4x5m7acsM8pnVg"/></column></grid><grid><column width-ratio="0.561411"><img name="CleanShot 2026-05-18 at 17.32.16.png" alt="图片展示了飞书群聊界面，用户发送“" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=MjE4NTUzMDNkNWE5YWIxMzI5OWVmMTU4Yjg2MTYwNjhfNWVkMzViNTIzOGVkOGQxNjBmZDAzNDkxNjJlNDQ0ZDFfSUQ6NzY0MTgzNTUwNjI3MTQwNzMxNV8xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM" mime="image/png" scale="0.715686" src="D00gbtCiTomFqrxmFCTcVJiCnPd"/></column><column width-ratio="0.438589"><img name="CleanShot 2026-05-18 at 17.32.41.png" alt="图片展示了飞书群聊界面，群名为“frontend slides整合”，成员有Napoleon（Zara&#39;s Claude Code）和张睿。群聊中，Napoleon以智能体身份发送消息“群已建好。@我 + 任意消息开始对话。”，并附有表情。该图片对应文档中““多session管理：一个会话=一个session，取代terminal tabs”部分，直观呈现了使用Claude Code/Codex在飞书里创建群聊、管理会话的操作效果，与上下文介绍的多session管理功能相契合。" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=ZDUyNjZmMjczZTQ0NzlhNTk1NGE2NWQ5ZmY2ODg3NmVfZjViMDRiZDhkMDM2NDk2ZGRiNjg5OWU0OGZhNzM0ZDJfSUQ6NzY0MTgzNTUwNzk5MDk3MzM3Ml8xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM" mime="image/png" scale="0.592532" src="VrP0bgV7PoB6CSxrDlScsAJXnZb"/></column></grid><br/>可以给所有带Claude Code的群加上标签，更方便一键找到：<grid><column width-ratio="0.517015"><img name="CleanShot 2026-05-19 at 21.15.20.png" alt="图片展示了飞书群聊界面，群名为“Napoleon (Zara&#39;s Claude Code)”，成员2270人。群内有“消息”“文档/资料”“图片/视频”等标签栏，当前选中“消息”标签。群聊中显示了Claude Code的回复内容，包括Bundle copy、本地测试期软链等信息，还列出了Phase A计划的两条任务。右下角有“设置”按钮，其下拉菜单中“标签”选项被红色框突出显示。该图片与文档中“多session管理”部分内容相关，直观呈现了给带Claude Code的群加上标签的操作界面。" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=YjUyODMxYjU5N2M1OWJhODk1MzgxNTc1YmQ4YTBlMzdfMjJlMTI4NDAzNzI4NTQyNWRjMWJkMGEwYjA3NDI0MjdfSUQ6NzY0MTgzNTUwODEwMDIwNTUxM18xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM" mime="image/png" scale="0.590615" src="GlChby5VcoKZXKxPYgHcr7Yynih"/></column><column width-ratio="0.482985"><img name="CleanShot 2026-05-19 at 21.16.22.png" alt="图片展示了飞书界面中Claude会话管理的示例。左侧为飞书消息列表，其中“Claude”标签下有多个会话记录，如Napoleon（Zara&#39;s Claude Code）发送的图片、CC for design、frontend slides整合等话题群聊。右侧是Claude的聊天界面，显示了不同会话内容。该图片与上下文紧密相关，直观呈现了文档中提到的“多session管理：一个会话=一个session，取代terminal tabs”功能，即在飞书里用会话管理，一个群=一个project，一个thread=一个session，且可自动创建群聊。" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=NWQ1NjA4N2E0N2Q1M2RjNTFhZGY4ZDU4MWI5OTA2YzdfOTdjMmZmZjEwOGVlYTk3YjlkNTdkODRhMGY3MGUyMDlfSUQ6NzY0MTgzNTUwOTk1Nzg1NjQ1OF8xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM" mime="image/png" scale="0.610368" src="WKV0bvFAAoU4DexFSfycQJYFn0e"/></column></grid></td></tr></tbody></table>

## 更丰富的表达：Claude Code/Codex可以突破纯文字限制，用富文本/多媒体跟我沟通

<table><colgroup><col/><col/></colgroup><tbody><tr><td><b>Before</b></td><td><b>After</b></td></tr><tr><td>Claude Code/Codex仅用文字的方式跟我沟通，经常是一大堆文字，不愿意看<img name="CleanShot 2026-04-21 at 16.18.47@2x.png" alt="图片展示的是Claude Code相关代码及文档内容。上方代码部分包含按钮相关代码，如按钮文本版本、使用 button as buttons等。下方文档内容提到文档评论自动回复、emoji反应等特性，还介绍了分享上游版本的原因" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=MWFkODc5M2I4YThlM2RiOWIyNzE5Y2ZlZDA5M2I0OGNfMDllOTI3OTIyMTljY2Y1ZTAwOTM0MTYzM2I0MWRhNjVfSUQ6NzY0MTgzNTUwNjU5MDI1NjMxNF8xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM" mime="image/png" scale="1.000000" src="ZJfobUwJaoN7lJxZmkAc7fSEn6f"/></td><td>Claude Code/Codex可以给我发送图文混排的消息<img name="CleanShot 2026-04-21 at 14.07.28@2x.png" alt="图片展示的是飞书界面中Cla addCriterion图片展示的是飞书界面中Claude Code发送的“产品开发流程图”消息。消息内容为“这是我用 Excalidraw 画的流程图，展示从想法到发布的三个核心步骤”，并配有流程图，图中包含“想法”“构建”“发布”三个步骤，箭头连接各步骤。消息底部有“想法→构建→发布”的文字标识。该图片与文档中“更丰富的表达：Claude Code/Codex可以突破纯文字限制，用富文本/多媒体跟我沟通”内容相关，直观呈现了Claude Code发送图文混排消息的能力。" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=YTZhOTU1NzdhOWFjN2QwN2E5YjljNjY2NjA3NTY3ZmRfNDgyZTE5ZDgwMTg5NTc1MGUyNjMzMDI2NzA4NDI0ODBfSUQ6NzY0MTgzNTUwNzYxMzQ1MzI3Nl8xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM" mime="image/png" scale="1.000000" src="DmlMblunYoHlYqxhlPicFxrgn6g"/><br/>可以给我发一个表格，并渲染出来<img name="CleanShot 2026-04-21 at 14.01.11@2x.png" alt="图片展示的是飞书群聊界面，群名为“Zara&#39;s CC”，成员有Zara&#39;s Claude Code机器人等。群聊中，Zara&#39;s Claude Code机器人回复张睿关于标题hallucinate的问题，给出最终结果，即在“~/follow-builders/prompts/summarize - tweets.md”文件中新增了一张硬编码表，每个handle对应固定的英文头衔和中文头衔，直接查表用，不再推断。该图片与上下文介绍的Claude Code/Cod可 addCriterion图片展示了飞书群聊界面，群名为“Zara&#39;s CC”，成员有Zara&#39;s Claude Code机器人等。群聊中，Zara&#39;s Claude Code机器人回复张睿关于标题hallucinate的问题，给出最终结果，即在“~/follow-builders/prompts/summarize - tweets.md”文件中新增了一张硬编码表，每个handle对应固定的英文头衔和中文头衔，直接查表用，不再推断。该图片与上下文介绍的Claude Code/C" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=NWU5YzNkZjNjOGIyNzAwYWFiZDIzMzNhODg1M2YxMThfNTFmMmY5ZGU5OTc0OGEwOWFiNzEzNWIwMWYzMTZmOTdfSUQ6NzY0MTgzNTUwNTkyNzYyMTU5MF8xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM" mime="image/png" scale="1.000000" src="BJVHbqlSloeNKLxScFlcZTTWnFh"/><br/>可以给我发送一个长图，并且直接在飞书里查看<img name="CleanShot 2026-04-23 at 16.43.11@2x.png" alt="图片展示了飞书群聊界面，群名为“Zara&#39;s CC”，成员有“Zara&#39;s Claude Code”和“Claude”。群聊中，用户张睿回复“像素太低，3x分辨率版本发出去了，现在是2.3MB，应该够清晰了。去看看是不是好多了？”并发送了一张长图，图中是“今日速读”内容，包含文字和图片。该图片与上下文紧密相关，直观呈现了Claude Code/Codex突破纯文字限制，用富文本/多媒体与用户沟通的效果，是文档中“更丰富的表达”部分的示例。" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=NjNiM2U1ODZhN2MwM2EzMWUzMWFmZGMyYjRmMGI0MzVfYzc2NGEyYzNjZDQ0NWQzYmM0MDRkMmJlM2U3NjJmNzJfSUQ6NzY0MTgzNTUwNzczMDk3NTkzN18xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM" mime="image/png" scale="1.000000" src="IFvHbixoSoJhM1xwX6Ocb6TcnSe"/></td></tr></tbody></table>

## 更友好的交互：Claude Code/Codex可以给我发可交互的飞书卡片，而不是让我打字选择

<table><colgroup><col/><col/></colgroup><tbody><tr><td><b>Before</b></td><td><b>After</b></td></tr><tr><td>给我出题让我选择时，需要打字选择/键盘控制，不符合直觉，而且选择内容只能是纯文本<img name="CleanShot 2026-04-21 at 16.23.18@2x.png" alt="图片展示的是Claude Code与Codex接入飞书后，Lark Coding Agent Bridge实现的更友好的交互效果。在“Push fixes”任务中，Tab Out提出有三个待推送改动，即WeChat Articles友好名、LinkedIn /feed首页、首页标签用友好域名显示，询问是否一起推到GitHub。下方有“全部推送”“先不推”“Type something”三个选项，与文档中“给我出题让我选择时，需要打字选择/键盘控制，不符合直觉，而且选择内容只能是纯文本”的问题形成对比，体现了交互方式的改进。" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=MDg4N2VkNjczYTUwZWJkNmIxZjkyYmZmYjkwYTlkMjNfYTY2YzhhMDMwY2JmNjQ2M2ZiOWYwMGUzMzRiMDlkZmNfSUQ6NzY0MTgzNTUwODA4MzE5ODkzN18xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM" mime="image/png" scale="1.000000" src="Wk73bZNXToqmxPxRYLUcjR5hndb"/><img name="CleanShot 2026-04-21 at 16.24.13@2x.png" alt="这张图呈现了一段关于改善开发沟通体验的提问及对应解决方案的选项，提问者询问对方若要改善terminal的沟通带宽限制体验，最想解决的痛点是什么，给出了四个具体方向：一是通过自动生成的“改前vs改后”截图对比实现视觉对比；二是用Excalidraw等工具绘制架构图替代大段文字解释；三是改完前端后直接在对话里嵌入live preview；四是采用分层文档，将重要结论放最前、技术细节可折叠，最后还询问对方日常最有用的选项或是否有其他想法。" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=YmFhYmJiNmRmODlmNTNlMTM3ZTIzNTMwMTc0MDQzN2RfMmYzOTEyZDM0YzdhMzM4ZTNiZTU3Y2ZlMTgzM2IwZWZfSUQ6NzY0MTgzNTUwOTMxNjIwOTg4Nl8xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM" mime="image/png" scale="1.000000" src="BIjrbJ882o70ydxzlIrcCF1Mn4d"/></td><td>Claude Code/Codex发送可交互的卡片，通过按钮交互，更符合直觉<img name="CleanShot 2026-04-21 at 13.57.22@2x.png" alt="图片展示了飞书界面中Claude Code机器人发送的文档生成结果。上方显示“Zara&#39;s CC”及“Zara&#39;s Claude Code”等信息，下方蓝色背景区域显示“文档已生成”，内容为“Multi - Session 小白指南：当 AI Agent 住进 IM 里”，并有对OpenClaw Session体系的小白语言翻译及产品思考相关问题。下方还有“打开文档”按钮。该图片与上下文紧密相关，直观呈现了Claude Code发送可交互飞书卡片的效果，即通过卡片形式给出文档生成结果，符合直觉且更易读、方便反馈。" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=ZDIyYTY2MDYzMjViOTc5OWVhNDg0YmVlNjQ3ZThmYjNfMzZkZmJlZDI2MTRhOTkxMjlkOGQ4NmI0MDExYWY2YWJfSUQ6NzY0MTgzNTUwOTMyNjI4NTc5MF8xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM" mime="image/png" scale="1.000000" src="LKK1bEsWMoMLw8xV26Lcej6fn3f"/><img name="CleanShot 2026-05-18 at 17.34.10.png" alt="图片展示的是飞书Agent x会议界面中的一道多选题。题目为“Agent在替你听会，什么情况它应该立刻把你拉回会议？”，并说明这一题决定了Agent的“警觉度”与“打扰阈值”。选项包括A.我被@或直接点名问意见，B.议题切到我负责/熟悉的领域，C.决策即将形成或议题僵住，需要拍板，D.关键人物开口（老板/客户/决策方），E.自己写（可空），F.命中我预先标注的关键词或话题，G.出现冲突/情绪上升，可能要我下场缓和。其中A选项被勾选。" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=Mzg0ZmVjNDJjZmY2YWNjODMyZmNiZWI2ZWU3YWQ4YzlfZTc2ZmZlZDU5MTZjYmE1ZjdhMWI3MWMzMGFmZmRiOWRfSUQ6NzY0MTgzNTUxMDIwOTU2MzYwNl8xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM" mime="image/png" scale="1.000000" src="V6XHbOEXzoNgm3x1z5Lcoh78nrf"/></td></tr></tbody></table>

## 用飞书文档取代 Markdown，让 specs/docs 更易读、更方便给反馈

<table><colgroup><col/><col/></colgroup><tbody><tr><td><b>Before</b></td><td><b>After</b></td></tr><tr><td>给我写markdown文档，给反馈的时候还得用文字描述。<br/>比如Claude Code/Codex最开始给我写了个spec，写的是markdown的形式，首先markdown就很不容易读，而且也不方便打开。其次如果我有具体的反馈，还得手动描述“第几段第几行，怎么改”，非常麻烦</td><td>给我写飞书文档，给反馈的时候直接划词评论<img name="CleanShot 2026-04-21 at 16.26.38@2x.png" alt="图片展示的是飞书界面中Claude Code机器人处理的文档内容。上方显示文档标题“HTML Artifact Design: The Collision Skill”，并列出包含问题诊断、三阶段碰撞架构等信息。下方有“背景与问题”板块，阐述AI生成HTML存在的问题，如优化目标错、缺乏commitment等。图片与上下文紧密相关，直观呈现了Claude Code处理飞书文档的效果，即能以可交互的飞书卡片形式呈现文档内容，方便用户查看和管理。" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=OTQ2NmZiZjc4MDU2MjNjZDM0MjBlMTUyNTk3YjdhYWJfZDBhZjM5NDdjNWY3MWY0ZmM5YTlmNzY3MTQ0NTVlZWVfSUQ6NzY0MTgzNTUwOTM5NTkwMTM5OF8xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM" mime="image/png" scale="1.000000" src="OEi1btCK3ofsk5xVjz1czA7Qnle"/><img name="image.png" alt="该图片分为左右两个部分，主题围绕“Agent拍马屁的问题”展开，左侧是正文内容，指出很多AI Agent为迎合用户会不加判断地过度顺从，忽略提供真实、有价值建议的重要性，还说明了这类问题的成因及解决该问题的多方面方法，也提到Multi-agent的潜力；右侧是对话内容，显示某用户询问Zara的CC Multi-agent是否是解决该问题的最优解，Zara的CC随后明确表示Multi-agent并非最优解，该方案虽能通过批评“AI拍马屁”，但存在RLHF偏好污染等问题，还提出了更根本的训练调整方式及Multi-agent的现状与局限。" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=NzZlYmY1ZTE4MWRkNTU5NTMxM2UxYWZmYWRiNjJiYWVfMTY2MzA2OTYzNGY3MjkyMmQ2OWY3MTYzMDJkYmVhNzZfSUQ6NzY0MTgzNTUwODc3NTIwOTkyMF8xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM" mime="image/png" scale="1.000000" src="IQfbbV7xVoIihpxgVCXcnHqtn8c"/></td></tr></tbody></table>

## 飞书里收到的消息，一键转发给Claude Code/Codex处理

<table><colgroup><col/><col/></colgroup><tbody><tr><td><b>Before</b></td><td><b>After</b></td></tr><tr><td>飞书里的消息，需要手动复制或者截图分享给Claude Code/Codex</td><td>直接把飞书消息合并转发给Claude Code/Codex。比如用户的反馈、leader布置的任务等等，可以一键布置给Claude Code/Codex<img name="CleanShot 2026-05-18 at 17.35.27.png" alt="这张图片展示的是飞书中名为“Napoleon（Zara&#39;s Claude Code）”的智能体聊天会话记录，核心内容是内部设计师与该智能体交流PWA 3D icon库相关的内容，包括提及该icon库采用双套风格、可加载桌面等特性，设计师还反馈了WebFetch抓取不到内部细节的问题，以及给出相关使用建议，该智能体可整合处理这类工作内容，体现了Claude Code接入飞书后能便捷处理协作相关需求的作用。" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=Yzk5MDU2ODVhN2FhN2YzNGQwZmM1YjVhNzI3OTNlOWFfYTkyNWU1MDM1MWQxMTMzZWNhZjEzYTIxN2NkZjdiYjdfSUQ6NzY0MTgzNTUwOTIzMjM3Mjk1MV8xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM" mime="image/png" scale="0.285016" src="OtuTbWsTxoHFlLxqvyAcHVa3n7g"/></td></tr></tbody></table>



## 聊天记录完整保留，方便检索、回顾、分享

| **Before** | **After** |
|-|-|
| 关掉terminal之后，聊天记录就没有了，因此经常不敢关。Claude并不会保留完整聊天记录，只会保留我自己的prompts。聊天记录不能很方便地回顾、检索、分享 | 所有聊天记录都留存在飞书里，方便检索、存档、回顾、分享。  <br/>比如我经常想给别人分享我跟Claude Code/Codex的brainstorm过程，或者vibe coding的过程，可以直接合并转发历史聊天记录。 |



# 快捷配置-打造你心仪的飞书交互体验

如果还有什么想许愿的交互体验，欢迎评论！

在飞书里直接发斜杠命令，回车即可生效。下面按用途分组，**不在表里的斜杠会原样转给 Claude/Codex 处理**。

## ⚙️ 偏好设置

- `/config`  — 表单调整：消息回复方式（卡片 / 纯文本）、工具调用是否显示、并发上限、**群内是否需要at bot 才回复**

  ![图片展示的是Lark Coding Agent Bridge的偏好设置界面。界面中可调整bot行为偏好，如消息回复方式（卡片/纯文本）、工具调用显示（显示或隐藏）、并发上限（1 - 50）、run探活（0 - 120分钟）等。其中，消息回复方式为纯文本，工具调用显示为隐藏，并发上限为10，run探活为0分钟，群内是否需要@bot为是（默认）。该界面与文档中介绍的Lark Coding Agent Bridge偏好设置内容相关，直观呈现了可调整的设置选项。](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=ZTQ5MzJhZDMzNTc1OGY3OThjMmE0OTNkZTg5YjIxODJfNDkwYTM4N2YwYWI5MDg4NjZmMzVjNTg5MTVkZGFjM2FfSUQ6NzY0MTgzNTUwNzcyNjYwMTQxMl8xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM)



- `/timeout` — **当前 session** 的 run 探活（优先级高于 /config 的全局值）

  - `/timeout 15` 当前 session 设 15 分钟无响应自动 kill
  - `/timeout off` 当前 session 关闭探活
  - `/timeout default` 清掉 session 覆盖，跟随全局
- `/account` — 查看当前应用；`/account change` 换 appId / secret 并热重连

## 🗂️ 会话管理

- `/new`（或 `/reset`） — 清空当前会话，从零开始
- `/new chat [名字]` — 新建一个群（自动拉你和 bot 进去），继承当前 cwd 后开新会话
- `/resume [N]` — 列出最近 N 个历史会话，点按钮一键恢复
- `/status` — 当前 cwd / session / agent 状态卡片
- `/help` — 命令速查卡片（更新中，下图可能不全，以实际为准）
- `/account` 切换绑定的bot

## 📁 工作目录 & 工作空间

- `/cd <路径>` — 切换 Claude 的工作目录（会重置 session）
- `/ws list` — 列出所有命名工作空间（卡片 + 按钮）
- `/ws save <名字>` — 把当前 cwd 存为命名工作空间
- `/ws use <名字>` — 切到指定命名工作空间
- `/ws remove <名字>` — 删除命名工作空间

## ⏹️ 运行控制

- `/stop` — 终止当前正在跑的 Claude 任务（等同卡片底部 ⏹ 终止 按钮）
- `/reconnect` — 强制重连 WebSocket（网络抖动后 bot 没反应时用）

## 🧭 进程管理（同 app 多开场景）

- `/ps` — 列出本机所有 lark-channel-bridge 进程，**标识"当前回复的是哪个"**
- `/exit <id|#>` — 终止指定 start 进程（关自己 = graceful 退出；关别人 = SIGTERM）

## 🩺 诊断

- `/doctor [描述]` — 把最近日志 + 你的故障描述喂给 Claude 自助诊断，返回可能原因 / 关键日志 / 建议下一步



# 多 profile：分别运行 Claude 和 Codex

默认情况下，bridge 使用当前激活的 profile；可以通过 `profile use <name>` 切换。每个 profile 会维护独立的应用凭据、会话、工作目录和日志。只有在需要同时连接多个 PersonalAgent 应用，或分别运行 Claude 和 Codex 时，才需要创建多个 profile：

```Plain Text
lark-channel-bridge start --profile claude --agent claude
lark-channel-bridge start --profile codex --agent codex
```

例如只重启 Codex bot：

```Plain Text
lark-channel-bridge restart --profile codex
lark-channel-bridge status --profile codex
```

# **Claude 计费说明**

Bridge使用的是claude -p模式，自 **2026 年 6 月 15 日**起，Claude 订阅计划对 `claude -p` 和 Agent SDK 的使用将**独立计费**，不再占用原有对话额度。

各订阅档位获得独立的月度额度：Pro **\$20**、Max 5x **\$100**、Max 20x **\$200**，当月未用完不滚存。

订阅价不变。轻度使用无影响；重度使用 `claude -p` 跑脚本的同学可能更快触顶，超额需按 API 付费或升级套餐，建议提前评估用量。

官方公告：[Use the Claude Agent SDK with your Claude plan | Claude Help Center](https://support.claude.com/en/articles/15036540-use-the-claude-agent-sdk-with-your-claude-plan)





**如果有建议或者反馈，欢迎在**[**GitHub**](https://github.com/zarazhangrui/feishu-claude-code-bridge)**上提issue/PR！也欢迎加入**[**飞书反馈群**](https://applink.feishu.cn/client/chat/chatter/add_by_link?link_token=898n02fa-c8f3-473f-a29d-e999024ead4c)**！**



![图片展示的是Claude Code Feishu Bridge飞行社的二维码，用于加入该飞行社。上方有“反馈”标识，表明可在此反馈建议。二维码下方提示“Scan the QR code to join the group. This QR code is valid permanently”，表示扫描此二维码可加入群组，且二维码永久有效。该图片与文档中“如果有建议或者反馈，欢迎在GitHub上提issue/PR！也欢迎加入飞书反馈群”的内容相关，是加入飞书反馈群的入口。](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=YzhkMGY0MmE2MjZkNGZhM2Q2MTU1MzU0NGMwOWRiZDFfMmVjZjBlNWExZmU5MDNkZWNiOWRlN2RkMWYxZWY5NjVfSUQ6NzY0MjYzODUzOTkyMjEzMTk0Ml8xNzgyODI2OTI3OjE3ODI4MzA1MjdfVjM)