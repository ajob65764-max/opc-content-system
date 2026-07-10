---
name: opc-content-system
description: Build and run a lightweight One Person Company content workspace using persistent personal context, platform-specific templates, reusable outputs, and anti-AI writing rules. Use when the user wants to initialize or personalize an OPC content system, create publish-ready content for Xiaohongshu, Douyin, WeChat Official Account, WeChat Channels, or Zhihu, adapt one source into multiple platform versions, save finished content into an Outputs structure, or turn repeated content patterns into reusable templates.
---

# OPC Content System

把用户的长期背景、真实素材和平台规则组合成可直接发布、可保存、可复用的内容成品。

## 判断任务类型

先判断用户要做哪一种任务：

1. **初始化工作区**：复制 `assets/starter-workspace/` 到用户指定目录。
2. **填写长期背景**：完善 `About_me/about-me.md`、`About_me/my-company.md` 和 `About_me/anti-ai-writing-style.md`。
3. **单平台创作**：生成小红书、抖音、公众号、视频号或知乎成品。
4. **一稿多平台**：把同一份真实素材分别改写成两个或更多平台版本。
5. **复盘与沉淀**：根据用户明确认可或重复验证的结构更新模板。

不要把简单的单篇创作扩展成复杂工作流。

## 初始化工作区

用户要求创建或安装 OPC 工作区时：

1. 让用户指定目标目录；未指定时，在当前工作区创建 `opc-content-workspace/`。
2. 复制 `assets/starter-workspace/` 的内容，不移动技能自身文件。
3. 目标目录存在时，先列出冲突；默认只添加缺少的文件，不覆盖、不删除原文件。
4. 告知用户工作区位置，并引导其填写三个 `About_me` 文件。

## 建立长期背景

创作前优先读取当前工作区中的：

- `About_me/about-me.md`
- `About_me/my-company.md`
- `About_me/anti-ai-writing-style.md`

如果文件仍是空白模板，进入引导填写模式。每次只问一个容易回答的问题，依次确认：

1. 用户是谁、从事什么；
2. 正在做什么内容或业务；
3. 主要服务谁；
4. 当前重点平台与目标；
5. 能提供的真实素材；
6. 不喜欢的表达和明确禁区。

只写用户真实回答。不确定的内容标记“待补充”，不自行编造。修改长期背景前先说明准备写入什么；保留已有有效内容。

## 单平台创作

只读取当前任务对应的参考文件：

| 平台 | 必读参考 |
| --- | --- |
| 小红书 | `references/小红书图文模板.md` |
| 抖音 | `references/抖音短视频模板.md` |
| 公众号 | `references/公众号文章模板.md` |
| 视频号 | `references/视频号短视频模板.md` |
| 知乎 | `references/知乎回答与文章模板.md` |

同时读取当前工作区的个人写作规则；没有个人规则时读取 `references/反AI味写作规则.md`。

执行顺序：

1. 提炼任务、目标读者、平台、核心观点、真实素材、成功标准、必须保留和明确不要。
2. 信息足够时直接创作；关键事实缺失时最多询问 5 个问题，不重复询问已知信息。
3. 优先使用用户的原话、经历、案例和数据，不编造身份、结果、客户案例或收益。
4. 根据平台模板输出完整成品和必要的发布辅助信息，不只给建议或提纲。
5. 检查标题与正文一致、事实边界清楚、表达自然、没有夸张承诺和无关营销。
6. 当前信息涉及可能变化的平台规则、政策、价格、医疗、法律或金融事实时，先核实；无法核实时明确标注。

## 一稿多平台

用户要求两个或更多平台版本时，读取 `references/一稿多平台改写模板.md` 及所有目标平台参考。

先建立内容母稿，固定：

- 核心事实；
- 唯一核心观点；
- 目标人群；
- 真实经历与数据边界；
- 希望读者采取的动作。

再按平台重新组织标题、开头、结构、语气和结尾。不要只缩短长度或替换平台名称。抖音与视频号不能使用完全相同的脚本，公众号与知乎不能简单复制。

## 保存交付物

当前工作区存在 `Outputs/` 时，把正式成品保存到对应平台目录：

```text
Outputs/小红书/
Outputs/抖音/
Outputs/公众号/
Outputs/视频号/
Outputs/知乎/
```

使用文件名：`日期-平台-选题名称-版本.md`。

文件顶部记录：

```text
状态：草稿/待审核/已发布
平台：
选题：
目标读者：
发布日期：
数据记录：
复盘结论：
```

不覆盖已发布文件或同名版本。发生冲突时创建下一个版本。当前工作区没有 `Outputs/` 且用户没有要求写文件时，在对话中交付完整成品并说明尚未保存。

## 沉淀与维护

- 用户明确指出长期写作偏好时，先修改当前内容；得到确认后再更新长期规则。
- 某种结构被用户认可或重复使用两次以上时，建议沉淀为模板。
- 未经用户同意，不修改长期背景或原平台模板。
- 新模板优先创建新版本，不覆盖旧模板；失效模板先标记“停用”。
- 不保存密码、证件、客户隐私或未脱敏商业机密。

## 完成交付

最终交付必须包含：

1. 可直接使用的完整成品；
2. 平台所需的标题、封面、字幕、摘要、话题或拍摄建议；
3. 简短的发布前检查结果；
4. 已保存文件的准确位置，或明确说明未保存原因；
5. 仅在确有复用价值时提出模板沉淀建议。
