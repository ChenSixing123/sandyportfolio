<title>C2 课前引入：从微信读书划线，到业务 Skill 的理解</title>

<callout emoji="💡">
**课前引入定位：**这个案例不是为了讲“读书笔记整理”，而是用一个低风险、容易理解的个人场景，先让大家看懂 Skill 的本质：把一个重复出现、规则清楚、需要稳定产出的工作流程，沉淀成可复用的 AI 工作能力。后面会自然过渡到正式内容：**Skill 构建 & 业务能力沉淀**。
</callout>

**Codex 不只是一个“帮我写东西”的工具，它也可以把一套固定工作方法沉淀下来，变成下次可以继续调用的能力。**

因为很多业务工作不是一次性的，而是每周、每月都会重复发生：整理数据、写周报、做复盘、筛选达人、生成脚本、输出汇报、追踪行动项。如果每次都重新写 Prompt，效率会提升一点，但方法论没有留下来；如果把流程沉淀成 Skill，团队就可以稳定复用同一套标准。

# 【问题痛点】先从一个轻量场景理解 Skill

我先从一个个人场景讲起。

我是微信读书的高粘性用户，最近读了腾讯研究院的**《从超级个体到超级团队》**，留下了 23 条划线。单看这些划线，它们只是一些零散句子：当时觉得有启发，但过一段时间再回头看，很难立刻想起它们之间的逻辑，也不方便拿去分享。

<grid>
<column width-ratio="0.500000">
<callout emoji="😅">
**原始状态**
- 23 条划线散落在微信读书里。
- 每条划线本身有价值，但缺少结构。
- 不方便整理成分享稿。
- 如果手工整理，需要重新复制、分类、总结。
</callout>
</column>
<column width-ratio="0.500000">
<callout emoji="😀">
**使用 Skill 后**
- Codex 通过 Skill 读取划线和感想。
- 可以查看我的书架，知道我的阅读偏好，并给我推荐相关书籍
- 帮我把笔记内容进行罗列整理，便于我进一步整理读书笔记分享稿
</callout>
</column>
</grid>

<grid><column width-ratio="0.500000"><p><source href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=YjZkOTk0N2JhYjIzODdiNTVjOGEyOGM0MzAyZDBkYjRfM2Y0YTcxYzRhYzU0NzdjYjMxYTQ3NDdjZWNlNzM0NjlfSUQ6NzY0ODg3ODQ1NDM2ODI5MjAzMF8xNzgyODI3NjkzOjE3ODI4MzEyOTNfVjM" mime="application/pdf" token="IpT3bKLu5obdQHxXCbxc03w4nnh"/></p><img name="b8a6bcaf842a67299e1f65150040c0b1.jpg" alt="图片展示的是微信读书“WeRead skills”功能界面。上方显示“已选择23个”笔记，有“取消”选项。中间部分呈现“腾讯研究院”笔记，标注“在读 - 共23条笔记”“时长44分”，并有“连接纸书书”“图片模式”“搜索笔记”“导出笔记”等操作按钮。下方是笔记内容，如“成熟企业的AI转型和初创团队的AI原生，都遵循着同一个底层逻辑”等，每图片与上下文介绍的微信读书“WeRead skills”功能相契合，直观呈现了其笔记管理及分享功能。" crop="[0.000000,0.060800,1.000000,1.000000]" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=ZjU0MDFhZWFiYjZlYmYyZjFkZTk2MGUyNmVkODIzZThfNWM3NmRlZjZlNGQ2NTg4NDg5OWViZmRlZjcxYWY4ODZfSUQ6NzY0ODg3OTM3ODg4MTA3MjExNV8xNzgyODI3NjkzOjE3ODI4MzEyOTNfVjM" mime="image/jpeg" scale="0.280063" src="SMfRbnr0qox5IBxkA7icHX1ZnDC"/></column><column width-ratio="0.500000"><p>但最近微信读书做了一个 <b>"WeRead skills"</b></p><p>它可以把查看你的书架、统计你的阅读数据、帮你找到你某本书的划线以及你自己的感想、还可以帮你推荐符合你偏好的书籍！</p><img name="image.png" alt="图片，介绍微信读书助手“WeRead”的能力。它通过Agent API Gateway调用微信读书接口，提供搜索、书架、笔记、书评等功能。支持搜索书籍、查看书籍信息、书架管理、阅读统计、笔记划线、章节热门划线、书籍点评、推荐好书等，每个功能有用户示例和详细说明，如搜索书籍示例为“帮我搜一下三体”，查看书籍信息示例为“这本书有多少章？”。" caption="截取自skill.md&#xA;" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=ODJkZmUwODQxYjQ5Y2RiYTIyMDI1ZWM4ZWYwYmMzOGZfNTliZGY2MGI3OWI0YWU4Njg5NjUzNGE5MjVkNGM3N2JfSUQ6NzY0OTU2ODc1Mzc5MzYxNzA4N18xNzgyODI3NjkzOjE3ODI4MzEyOTNfVjM" mime="image/png" scale="1.000000" src="XoLnbN6egomLi2xQw9McmUmpn7b"/><p></p><p>点击下面link进行配置：</p><p>https://weread.qq.com/r/weread-skills</p></column></grid>

<grid>
<column width-ratio="0.417055">
![图片展示的是微信读书“image_id-1的配置结果页面。页面显示了已处理1m27s的提示，显示“weread-skills”已成功连接并能调用微信读书API。书架有185个 自动生成](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=ZjdmYjUxZDdkZWM3NTAxODNlY2ZmNjE4ODI5OGEwYTZfMDQxNDhlMjZkMzg2OWRmMWMxYzFkYzRjNDU3YWM0YmNfSUQ6NzY0ODg4MTIxNjkwNDgwOTY5M18xNzgyODI3NjkzOjE3ODI4MzEyOTNfVjM)
</column>
<column width-ratio="0.582945">
![图片展示的是腾讯研究院公众号文章《从超级个体到超级团队》部分内容。左侧为文章正文，右侧是作者Sandy的评论。评论中提到AI让“超级个体”重新出现，强调了AI在工作流程、能力边界跃迁、自主性、影响力等方面的作用，以及“四因缺一不可”的解释。评论还指出超级个体并非万能，个体能力被AI放大后，依然存在局限性，如无法替代团队的创造力、信任度等。该图片与上下文介绍的微信读书“WeRead skills”功能相呼应，体现了AI在个体与团队关系中的作用。](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=OGVkZDU3ZTk0ZWJmODlkZjYxMzIzMWI1YmYzYWJhMzRfN2ExYWFiNTVlYzNjMWQxMjRlM2JhYWE0ZmY5ZmQ5OWNfSUQ6NzY0ODg4MTMxOTExNjAwMDQ5OV8xNzgyODI3NjkzOjE3ODI4MzEyOTNfVjM)
</column>
</grid>

<grid>
<column width-ratio="0.487365">
![图片展示了一篇关于《纳瓦尔宝典》的读书笔记内容。笔记中列出了书中的71条划线，其中7条带有个人感想或点评。每条划线包含了上下文的关系](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=NDZiMzI4YTJiNWFmMDg2OGJjMmVhMGE4OGM3NGFhNWVfMmY0MTJiZGZlYjVlOTRiYmExMWQ1Mzk2Njc1NWY2MmNfSUQ6NzY0OTU3NTAyNTE5NjI1NjQ2OF8xNzgyODI3NjkzOjE3ODI4MzEyOTNfVjM)
</column>
<column width-ratio="0.512635">
![图片展示了一段对话内容。用户询问微信读书AI根据其阅读习惯推荐三本书。AI推荐了《系统之美》、《如何快速了解一个行业》、《东京贫穷女子》三本书，并对每本书进行了简要介绍，如《系统之美》适合避开书架已有书后挑，可提升业务技能；《如何快速了解一个行业》适合企业内训、社媒复盘等，可快速搭建行业地图；《东京贫穷女子》可补现实观察线，关注个体选择背后的结构性困境。还给出了阅读建议，如先读《如何快速了解一个行业》，再读《系统之美》，最后读《东京贫穷女子》。](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=YzkwY2Q4NzJhYmI4ZGY2Y2ViZjAwOTAzYjM2NTQ5NDdfZDBlZThkZWYwYWE5OTI4ZjM2MDgyMzhhNjk3ZjZlNDVfSUQ6NzY0OTU3NTk5MjY5NjI2MTgxMl8xNzgyODI3NjkzOjE3ODI4MzEyOTNfVjM)
</column>
</grid>

# 【Skill 定义】从一句 Prompt 到一个能力包

Skill 不是一句 Prompt，而是一个小型能力包。里面既有**主流程说明**，也可以放**业务口径、参考资料、固定模板、脚本和输出样式**。

**下面我们来看看一些 skill 文件包里面到底都有什么？**

![图片展示了微信读书技能文件包中的部分文件。文件以`.md`结尾，包括`book.md`、`discover.md`、`notes.md`等，还有一份名为`SKILL.md`的总指挥文件。这些文件位于`references/`目录下，是技能文件包的组成部分，用于存放字段口径、分析框架、接口说明、判断标准等业务知识，是技能文件包中业务知识库的体现，与上文介绍技能文件包组成部分的内容相呼应。](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=ZTNmMGM2YThjNmZhNTI4ZGVlYjg3M2ZiM2E3ZmI4ZDFfNjQ5YmVlMWQxMmZkNjg5MGU0Yjc3Y2QyYjY4OGNiMTFfSUQ6NzY0OTU3Njc3NDk2Nzg1NjMyNF8xNzgyODI3NjkzOjE3ODI4MzEyOTNfVjM)

![图片展示的是AI热点新闻skill文件包的内容界面。左侧文件目录中，`SKILL.md`文件被红色框线突出显示。右侧窗口显示了`SKILL.md`文件的具体内容，包括名称“AI HOT”、描述（介绍可查询AI资讯的功能及相关关键词）、先决条件（需带User - Agent，仅API端点）等信息。这与上下文提到的查看skill文件包内容相契合，直观呈现了`SKILL.md`作为AI热点新闻skill总指挥文件的具体设置。](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=ZGM0YjM0ZTJjZjQ0MjIzMzBmMTBiZmM2ZWEyOTQ2YjJfOTA4YjY2NGRkM2YyNzdkODEzNTBhYmVmYmU1ZjcwY2FfSUQ6NzY0OTU3NzQ2Nzc5NTkxNzc4NV8xNzgyODI3NjkzOjE3ODI4MzEyOTNfVjM)

![图片展示了“hv - analysis”技能文件包的内容。左侧是文件目录，包含references、scripts、met_to_pdf.py和SKILL.md等文件夹及文件。右侧是SKILL.md文件内容，标题为“横纵分析法深度研究”，介绍了该技能由数字生命卡兹林提出，融合了时 - 时分析、社会科学学科分析等研究方法，适用于产品公司概念/人物的通用研究框架，核心原则为：纵向追时间度、横向追维度度，最终交出分析报告。该图片与上下文介绍技能文件包组成部分及业务化理解的内容相关。](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=MTliM2U3YjMzMjM1Nzg5NGRmMmI4YWY5ZDBlMzRmNmJfY2MzNzIwY2YyNjEwNzFlNDg2MTE0ZjI5OWMxNGRiNjFfSUQ6NzY0OTU3Nzg1NTc0Nzg2OTkxM18xNzgyODI3NjkzOjE3ODI4MzEyOTNfVjM)

![图片展示了卡兹克公众号长文写作技能文件包的目录及SKILL.md文件内容。目录中“references”“content_methodology”“style_examples”“SKILL.md”被绿色框突出显示。SKILL.md文件中，name为“khazix - writer”，description介绍了该技能是卡兹克公众号的个人写作风格skill，当用户需撰写公众号文章、写稿子、续写文章等时使用，强调触感和情感表达。该图片与上下文介绍技能文件包组成部分的内容相关，直观呈现了技能文件包中“SKILL.md”文件的位置及部分关键信息。](https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=YzI5NWJjNjY4MzllM2QzN2ZhYTI3M2JmNGU1YmZmYjBfYmFhMzYxZTRjOWVlZWZhNTM4YzdmZmZiN2VkNzEwZGZfSUQ6NzY0OTU3ODM0NDcxMTY3MDc1Nl8xNzgyODI3NjkzOjE3ODI4MzEyOTNfVjM)

| 组成部分 | 业务化理解 | 作用 |
|-|-|-|
| `SKILL.md` | 总指挥 | 告诉 Codex 这个 Skill 什么时候使用、解决什么问题、按什么流程工作。 |
| `references/` | 业务知识库 | 放字段口径、分析框架、接口说明、判断标准。Codex 需要深入理解时再读取。 |
| `assets/` | 固定交付模板 | 放报告模板、看板模板、样式文件、示例素材，用于稳定生成最终成果。 |
| `scripts/` | 稳定执行工具 | 放可执行脚本，用来处理重复、稳定、容易出错的计算或转换任务。 |
| **`agents/openai.yaml`** | **展示信息** | **告诉 Codex 界面这个 Skill 叫什么、能做什么、默认怎么调用。** |

`references` 和 `assets` 的区别

<table><colgroup><col/><col/><col/></colgroup><thead><tr><th colspan="2" vertical-align="top">一句话理解</th><th vertical-align="top">使用方式</th></tr></thead><tbody><tr><td colspan="2" vertical-align="top"><code>references/</code><br/><b>给 Codex 看</b>的「业务参考资料」。</td><td vertical-align="top">当 Codex 需要理解字段、指标、诊断框架、报告结构时读取。<br/>例如：什么是核销率、退款率怎么算、达人如何分层。</td></tr><tr><td colspan="2" vertical-align="top"><code>assets/</code><br/><b>给最终产物</b>用的「固定资源和模板」。</td><td vertical-align="top">当 Codex 需要生成稳定交付物时调用。<br/>例如：套用固定 HTML 数据看板模板，而不是每次重新设计版式。</td></tr></tbody></table>

<callout emoji="💡">
p.s. 实际的微信读书 Skill 当前结构更轻量，很多说明文件直接放在根目录下**，并不一定严格分成 `references/` 和 `assets/`**。这里展示的是更标准、更适合教学的组织方式。
</callout>

# 【使用步骤】一般情况下，我是如何使用 skill 的？

**人 + codex (AI agent)  + skill** 交互的工作流

<whiteboard token="YW0VwPABNh0PqcbJKFxcsLmanXb"></whiteboard>

<table><colgroup><col/><col/></colgroup><thead><tr><th vertical-align="top">阶段</th><th vertical-align="top">我会怎么做？</th></tr></thead><tbody><tr><td rowspan="3">安装前：<ul><li>发现问题</li><li>寻找skill</li><li>安装skill</li></ul></td><td>出现了一个<b>重复性</b>的需求任务场景，但是codex 或其他agents的<b>通用能力没办法稳定地解决这个问题</b>（或者说不符合我的要求），于是我想要找一个skill帮我解决</td></tr><tr><td vertical-align="top">我会在哪里找合适的skill帮我？<br/><b>官方🏬</b>：比如Workbuddy里面就有官方skill，Claude官方插件市场<br/><b>社媒📚</b>：小红书上面会有很多人推荐，看博主整理出的 skill 简介<br/><b>GitHub🔗：</b>直接在网站上搜索，重点看收藏🌟多的</td></tr><tr><td vertical-align="top">找到较为合适的skill，直接把链接发给codex，让其下载安装skill<br/>可以只装到项目级，这样就只有那个项目可以用，避免做不同项目时skill打架。<br/>少数skill需要配置Api，比如微信读书skill</td></tr><tr><td rowspan="3" vertical-align="top">安装后：<ul><li>查看skill能力边界</li><li>尝试skill的基本功能</li><li>基于skill的输出进一步延伸发散，直到你达到目的</li></ul></td><td vertical-align="top">查看这个skill的能力边界，我会做：<ul><li>打开skill.md 文件自行查看</li><li>直接问codex：“<em>这个skill可以帮我实现什么功能</em>”</li></ul></td></tr><tr><td vertical-align="top">直接在codex聊天窗口输入你的需求，等待skill完成任务</td></tr><tr><td vertical-align="top">如skill的结果不够满意，你还可以继续让codex干活，直到你达到自己的目的<ul><li>比如微信读书笔记整理这个例子：WeRead Skill 其实只能帮助我把划线笔记和感想找到，这是这个 skill 的能力边界。但其实我是想要把这些笔记更好地整理成分享稿，然后进行传播。我就可以继续跟 Codex 说：<em>“把划线整理成</em><em><u>思维导图和分享稿</u></em><em>。” </em></li></ul><grid><column width-ratio="0.502332"><img name="image.png" alt="图片展示了腾讯研究院公众号 *Sandy* 发表的微信读书笔记内容。笔记标题为“从超级个体到超级团队”，作者是 *Sandy* ，处理时间为3m 25s。笔记 自动生成 addCriterion&lt;qa:image&gt;&lt;/qa&gt;" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=NDRhNWVkOGMzNDcwYzkyNDM2YzRlZjQzZGFmOWFkMWVfZjA4NDU4YjE5ZTQzZTZhNmMxNTUzNGZmM2UwNzU3YmFfSUQ6NzY0OTYwNjMxOTkwOTYwNDI4Ml8xNzgyODI3NjkzOjE3ODI4MzEyOTNfVjM" mime="image/png" scale="0.122578" src="RkezbpRHPoAXXYxveohcD6UrnNd"/></column><column width-ratio="0.497668"><img name="image.png" alt="图片展示的是微信读书界面，左侧显示书籍《从超级个体到超级团队》的思维导图式笔记概览，色彩丰富，节点众多。右侧为该书具体段落内容，是关于AI对个体和团队影响的思考。结合上下文，此图与微信读书笔记整理相关，可能是用户使用微信读书skill找到的划线笔记和感想内容，展示了从微信读书获取笔记后，可进一步向Codex提出如整理成思维导图和分享稿等需求的应用场景。" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=YTk3N2M4Y2VlM2RiYzcxMjljMmYxZmJlZmYwYzZlMmVfMjg2NzY0Y2UyYzQ1MjkxOWNlMzlkN2E1ZDI0M2I5ZjRfSUQ6NzY0OTU3OTg0NDE5NTkyOTA0NV8xNzgyODI3NjkzOjE3ODI4MzEyOTNfVjM" mime="image/png" scale="0.121078" src="IjGWbnLWmosgGXxU83Ec69FXnpW"/></column></grid></td></tr><tr><td rowspan="2" vertical-align="top">进阶用法：<ul><li>迭代出更独属于你的skill</li><li>探索出你的skill组合拳</li></ul></td><td vertical-align="top">Skill进一步完善：<br/>比如说你在 GitHub 上下载了一个关于内容营销、达人运营相关的 skill，但是你会发现它里面的有些内容不太符合你的业务需求。你可以继续跟 Codex 说：<em>“根据我前面跟你交互聊天的信息，</em><b><em>你进一步帮我把这个原有的 skill 进行完善</em></b><em>。”</em></td></tr><tr><td>不过像微信读书这种，本质上是连接外界 APP，官方发布的 Skill，不建议直接修改。那当你发现你的任务只用这一个 Skill 没办法满足的时候，可以考虑去探索<b>一套 Skill 组合拳。</b><ol><li seq="1"><b>微信读书 skill + Sandy Writer skill = Sandy风格的读书笔记</b><ul><li seq="1">从我的微信读书中，提取我划线的金句以及我的感受。</li><li seq="2">把读书笔记进一步用“我的风格”优化，包括一些特定的文风或格式。</li></ul></li></ol><img name="image.png" alt="图片展示了微信读书技能“微信读书笔记整理”的相关界面。左侧是技能介绍，包括技能名称、作者、技能描述 自动生成方式、技能描述等信息，还列出了技能的2个文件，如“从超纲个体到团队的Sandy分享稿.md”等。右侧是技能的详细内容，包含技能介绍、技能使用示例、技能使用说明等，如技能介绍中提到该技能可将微信读书笔记整理成思维导图和 自动生成方式、技能描述等信息，还列出了技能的2个文件，如“从超纲个体到团队的Sandy分享稿.md”等。右侧是技能的详细内容，包含技能介绍、技能使用示例、技能使用说明等，如技能介绍中提到该技能可将 自动生成方式、技能描述等信息，还列出了技能的2个文件，如“从超纲个体到团队的Sandy分享稿.md”等。右侧是技能的详细内容，包含技能介绍、技能使用示例、技能使用说明等，如技能介绍中提到该技能可" href="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/authcode/?code=ZmM5ZDE1NDA3NWQ1ZGU2ODA1ODk3NDgxMDI5OTJiZGFfNmJhOWY0Y2Y1ODI5MjRhYjZmZGY1NmVkOTNkNmQ1YjFfSUQ6NzY0OTU4NzAxNzcwMTE2NjAyMl8xNzgyODI3NjkzOjE3ODI4MzEyOTNfVjM" mime="image/png" scale="0.205802" src="USarbSQujojY6rxiq88cEGdJnJd"/><ol><li><b>微信读书 skill + </b><b>beautiful html skill </b><b>= 读书会分享汇报材料</b></li></ol><br/><cite type="user" user-id="ou_71308a7afc28106df1a8a70db4602f06" user-name="陈思行"></cite>整理为下面的html网页供大家快速阅读<br/>https://zara-html-template-guide.vercel.app/super-individual-to-team-sandy.html</td></tr></tbody></table>

# 【业务价值】从个人案例过渡到企业业务场景

<callout emoji="📌">
Skill 的价值，就是把这些**原本依赖个人经验**的工作方法固定下来，让**团队可以稳定复用**。
</callout>

阅读划线只是一个低风险练习，真正要带大家进入的是企业内部的高频业务场景。

<grid>
<column width-ratio="0.500000">
**一次性 Prompt 的常见问题**
- 每次都要重新解释背景。
- 不同人写出来的提示词不一致。
- 输出格式不稳定。
- 洞察容易停留在表层。
- 业务口径和质量标准无法沉淀。
</column>
<column width-ratio="0.500000">
**Skill 要解决的问题**
- 把高频任务固定成标准流程。
- 把优秀业务人员的方法论写进能力说明。
- 让输出结构稳定、可检查、可复用。
- 把个人经验转化为团队资产。
- 让 Codex 更像一个懂业务流程的协作者。
</column>
</grid>

<callout emoji="✅">
刚才这个微信读书案例，是一个个人知识管理场景。接下来我们把同样的方法放到业务里：
如果每周都要做抖音投放复盘，每次都重新写 Prompt，其实就是在重复消耗。更好的方式，是把复盘边界、输入、流程、分析框架、输出形态和质量标准沉淀成一个 Skill。
</callout>

# 【推荐阅读】从超级个体到超级团队

《从超级个体到超级团队》这篇文章可以帮助企业内部同事理解：

**AI 不是只让某个员工变得更快，而是会改变团队协作和业务能力沉淀的方式。**

<cite type="user" user-id="ou_71308a7afc28106df1a8a70db4602f06" user-name="陈思行"></cite>整理为下面的html网页供大家快速阅读：

https://zara-html-template-guide.vercel.app/super-individual-to-team-sandy.html

| 文章洞察 | 放到企业业务里怎么看 | 和 Skill 的关系 |
|-|-|-|
| AI 会先放大个体 | 一线业务人员可以更快完成数据整理、复盘、方案起草和行动建议。 | Skill 把个人高效做法固化下来，避免只停留在“某个人很会用 AI”。 |
| 超级个体不是高产者 | 真正重要的是业务判断、问题拆解、证据链和交付闭环。 | Skill 需要写清楚判断框架，而不是只写“帮我生成报告”。 |
| 组织摩擦会限制产出 | 等待数据、反复对齐口径、重复解释背景，都会消耗业务效率。 | Skill 可以减少重复解释，让流程、口径和输出标准提前固化。 |
| FDE 思维值得借鉴 | FDE 的核心是靠近真实问题、快速交付、沉淀可复用方案。 | 业务人员也可以用 FDE 思维，把自己的场景沉淀成可执行的 Skill。 |
| 超级团队承接长期价值 | 团队价值不是每个人各自提效，而是形成共享的工作方法和复盘标准。 | Skill 是把个人经验升级为团队资产的一种方式。 |

# 一句话收束

刚才的案例展示了 Skill 如何连接真实数据，并把零散素材整理成结构化成果。

接下来我们不再停留在个人知识管理，而是进入企业业务场景。

<callout>
**今天的核心问题是：**如何把一个高频办公场景沉淀成 Codex Skill。正式案例会用社媒数据监控与投放复盘，讲清楚 Skill 的边界、输入、流程、框架、输出和质量标准。
</callout>

这个引入案例想让大家先建立一个共识：Skill 的价值不是多写一个 Prompt，而是把一个真实场景里的数据、流程、判断和输出标准沉淀成团队可复用的业务能力。微信读书案例是入口，社媒投放复盘才是我们接下来要正式拆解的业务版本。