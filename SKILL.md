---
name:pp-design-system
description:PP大王的个人设计与教学视觉系统。用于制作HTML页面、教程页面、教学页面、课程网站、个人网站、介绍页面、科普页面、Landing Page、图文卡片、公众号排版等设计任务。包含PP大王专属品牌DNA、场景规范与页面模板。
author: ESTHER不二 (esthersjw)
license: CC BY-NC-SA 4.0
repo: https://github.com/esthersjw/esther-design-system
---

> © 2026 ESTHER不二 (esthersjw) | CC BY-NC-SA 4.0
> 使用本 Skill 需署名原作者，禁止商用，修改后须以相同协议分享。

触发条件：当用户要求制作HTML网页、个人页面、教程页面、介绍型页面、landing page、活动页面、App型页面、作品集等任何前端设计相关任务时触发。也在用户说"做图文"、"图文卡片"、"小红书图文"、"文章转卡片"、"转成图文"、"做卡片"时触发。

## 使用方式（7步工作流）

### Step 1: 澄清需求
根据任务需要确认以下信息；如果用户已经提供，则不要重复询问：
1. 类型 —— 教程页面？教学页面？介绍/科普页面？活动页/Landing App/功能型页面？图文卡片？公众号排版？
2. 使用对象 —— 给谁看？学生、教师、公众还是其他人群？是否有明确年龄或专业基础？
3. 内容规模 —— 大概需要几个Section / 几屏？是否已有明确章节结构？
4. 素材 —— 用户是否已经提供文字、图片、数据、课程内容、截图或参考网页？
5. 硬约束 —— 必须保留什么内容？是否有指定尺寸、品牌色、课程视觉、设备适配或交互要求？

### Step 2: 读规范
1. 必读 `brand-dna.md`
   - 确认 PP大王 的品牌底层规范、视觉气质、配色、排版和组件语言。
2. 根据任务类型读取对应场景文件：
   - 教程页面 / 教学页面 / 介绍页 / 科普页
     → `references/scene-tutorial.md`
   - 活动页 / 分享页 / Landing Page
     → `references/scene-landing.md`
   - App / 功能型页面 / 工作台 / 看板 / 工具页
     → `references/scene-app.md`
   - 图文卡片 / 小红书图文 / 文章转卡片
     → `references/scene-cards.md`
   - 公众号排版 / 微信图文
     → `references/scene-wechat.md`
3. 如果任务同时包含多个场景，可以同时读取多个 reference 文件，不必只选一个。

### Step 3: 拷模板
优先从 `assets/` 中选择最接近当前任务的模板作为起点：
- 教程页面 / 教学页面 / 科普页面
  → `assets/template-tutorial.html`
- 活动页 / Landing Page / 宣传页面
  → `assets/template-landing.html`
- App / 功能型页面 / 教学平台 / 工作台 / 互动工具
  → `assets/template-app.html`
- 图文卡片 / 内容卡片 / 社交媒体卡片
  → `assets/template-cards.html`
原则：
- 优先基于模板修改，不从零开始重写。
- 如果现有模板与任务不完全匹配，可以在保留品牌视觉规则的前提下调整结构。
- 如果用户已经提供现成 HTML、网页代码或已有页面，则优先在用户现有内容上继续修改，不强制套用模板。
**从模板开始改，不从零写。**

### Step 4: 选布局组合
从 `references/layouts.md` 中选取 3~5 种布局模式，为每个 section 分配不同布局。

**每个 section 布局必须不同。**

（图文卡片模式：参考 `scene-cards.md` 中的推荐排版手法，为每页选择不同手法。）

### Step 5: 选组件填充
从 `references/components.md` 中选取组件填入各 section。

**硬规则：禁止使用任何HTML默认样式。** 所有引用块、列表、表格、卡片必须从 components.md 里选用对应组件的代码。不允许用默认 `<blockquote>`、默认 `border-left` 引用、无样式 `<ul>/<ol>`、默认 `<table>`。如果在 components.md 里找不到合适的，自己设计一个符合 brand-dna 规范的，但绝不能用浏览器默认样式。

### Step 6: 自检
对照 `references/checklist.md` 逐条检查：
- **P0 必须全过** — 任何一条不过就要改
- P1 应过 — 尽量满足
- P2 加分 — 锦上添花

（图文卡片模式：额外对照 `scene-cards.md` 底部的 Checklist；公众号模式：额外对照 `scene-wechat.md` 底部的 Checklist，逐项检查标题是否发生非语义断行或英文断词。）

### Step 7: 交付
输出最终 HTML 文件，确保可直接在浏览器打开。

## 场景类型速查

| 类型 | 场景文件 | 模板 |
|------|----------|------|
| 教程型/介绍型/科普型 | `references/scene-tutorial.md` | `assets/template-tutorial.html` |
| 活动页/分享会/Landing | `references/scene-landing.md` | `assets/template-landing.html` |
| App型/功能型 | `references/scene-app.md` | `assets/template-app.html` |
| 图文卡片/小红书图文 | `references/scene-cards.md` | `assets/template-cards.html` |
| 公众号排版 | `references/scene-wechat.md` | `assets/template-wechat.html` |

## 关键原则
- **从模板开始改，不从零写** — 模板已内置品牌变量和基础结构
- **每个 section 布局必须不同** — 避免单调重复，从 layouts.md 选不同模式
- **做完必须跑 checklist** — P0 全过才能交付

## 禁忌
严格遵守 `brand-dna.md` 的禁忌清单，不在此重复。核心底线：截图发 Twitter 不会被说"又是AI做的"。
