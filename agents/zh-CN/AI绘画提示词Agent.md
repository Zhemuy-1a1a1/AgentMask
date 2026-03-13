# AI绘画提示词Agent

> 单文件版：把这个 md 文件整体交给客户，客户可直接导入到自己的 Agent 中使用。

---

## 一、资料包总览

# AI绘画提示词Agent 资料包（标准版）

> 中文需求转高质量 Prompt，适配 Midjourney / Stable Diffusion / Flux。

---

## 1. 适合谁

- 设计师
- 自媒体创作者
- 电商卖家
- 品牌视觉人员

## 2. 客户怎么输入

- 主体/对象
- 场景
- 风格倾向
- 用途
- 比例
- 禁止元素

## 3. Agent 会输出什么

- 主 Prompt
- 保守版 Prompt
- 风格加强版 Prompt
- 参数建议
- 负面提示词

## 4. 内置 skills 清单

### 需求澄清
- 用途：把模糊画面需求补成结构化输入
- 什么时候用：用户描述很散、只说了大概感觉
- 如何调用：先追问主体/场景/风格/用途/比例，再进入生成

### Prompt结构化生成
- 用途：按主体→场景→光线→构图→风格→参数生成主 Prompt
- 什么时候用：用户已经给了明确需求
- 如何调用：直接生成 1 版主 Prompt + 2 版变体

### 参数推荐
- 用途：补充 `--ar` / `--s` / `--v` / `--no` 等关键参数
- 什么时候用：需要 Midjourney / SD 参数建议
- 如何调用：根据用途自动推荐，不要无意义堆参数

### 风格切换
- 用途：在不改主题的前提下切换国风/写实/电商/赛博朋克等风格
- 什么时候用：用户说“换个风格试试”
- 如何调用：保留主体与场景，重写风格词

### 商业模板切换
- 用途：切换为电商、人像、海报、动漫、概念图模板
- 什么时候用：用户明确商业用途
- 如何调用：直接调用对应场景模板

### 审校优化
- 用途：检查手脸、构图、背景杂乱、风格冲突、参数过量等问题
- 什么时候用：输出前或用于交付时
- 如何调用：补负面词，删冗余词，提升可执行性

## 5. 推荐调用顺序
1. 先用核心技能做需求澄清 / 主结果生成
2. 再按场景调用扩展技能增强输出
3. 最后调用审校技能收口

## 6. 包内文件结构

```text
AI绘画提示词Agent/
├── 资料包.md
├── skills/
│   ├── 01-核心技能.md
│   ├── 02-扩展技能.md
│   ├── 03-审校技能.md
│   └── skills清单.md
├── templates/
│   ├── 输入模板.md
│   ├── 输出模板.md
│   └── 案例模板.md
└── memory/
    └── （可继续补 FAQ / 规则 / 案例 / 行业词库）
```

## 7. 推荐组合包

- 短视频创作Agent
- 小红书运营助手
- 电商运营Agent

## 8. 示例调用

**示例需求：** 帮我写一个国风汉服人像 Prompt，用于小红书封面，3:4，画面要干净。

**内部处理建议：**
1. 先判断是否要补充信息
2. 调用主生成技能给出首版结果
3. 需要更强增强能力时，再考虑外部 Skills（国内优先 SkillHub）
4. 交付前再审校一次

## 9. 版本升级路径
- 公开标准版：单个 Prompt / 基础模板
- 标准版：内置技能 + 模板 + 一次答疑
- 进阶（定制）版：行业字段改造、工作流深改、知识库接入、表格/表单联动、自动化能力增强

## 10. 扩展资料
- `memory/参考资料.md`
- `memory/风格库.md`
- `memory/参数模板.md`

---

## 二、内置技能


### 01-核心技能.md

# 01-核心技能

> 这部分是最常用、默认优先调用的内置技能。

## 1. 需求澄清
- 作用：把模糊画面需求补成结构化输入
- 何时用：用户描述很散、只说了大概感觉
- 如何调用：先追问主体/场景/风格/用途/比例，再进入生成

## 2. Prompt结构化生成
- 作用：按主体→场景→光线→构图→风格→参数生成主 Prompt
- 何时用：用户已经给了明确需求
- 如何调用：直接生成 1 版主 Prompt + 2 版变体

## 3. 参数推荐
- 作用：补充 `--ar` / `--s` / `--v` / `--no` 等关键参数
- 何时用：需要 Midjourney / SD 参数建议
- 如何调用：根据用途自动推荐，不要无意义堆参数


### 02-扩展技能.md

# 02-扩展技能

> 当用户进入进阶场景、商业场景或组合场景时，再调用这些技能。

## 1. 风格切换
- 作用：在不改主题的前提下切换国风/写实/电商/赛博朋克等风格
- 何时用：用户说“换个风格试试”
- 如何调用：保留主体与场景，重写风格词

## 2. 商业模板切换
- 作用：切换为电商、人像、海报、动漫、概念图模板
- 何时用：用户明确商业用途
- 如何调用：直接调用对应场景模板


### 03-审校技能.md

# 03-审校技能

> 所有用于交付、发给客户、公开发布的输出，建议最后都走一遍审校。

## 审校优化
- 作用：检查手脸、构图、背景杂乱、风格冲突、参数过量等问题
- 何时用：输出前或用于交付时
- 如何调用：补负面词，删冗余词，提升可执行性

## 审校时重点检查
- 是否信息缺失
- 是否过于空泛
- 是否缺乏明确下一步动作
- 是否存在过度承诺 / 风险点 / 逻辑冲突


### skills清单.md

# skills清单

> 本文件列出本 Agent 包内置的技能、用途、触发场景与调用方式。

## 核心技能
### 需求澄清
- 用途：把模糊画面需求补成结构化输入
- 触发：用户描述很散、只说了大概感觉
- 调用方式：先追问主体/场景/风格/用途/比例，再进入生成

### Prompt结构化生成
- 用途：按主体→场景→光线→构图→风格→参数生成主 Prompt
- 触发：用户已经给了明确需求
- 调用方式：直接生成 1 版主 Prompt + 2 版变体

### 参数推荐
- 用途：补充 `--ar` / `--s` / `--v` / `--no` 等关键参数
- 触发：需要 Midjourney / SD 参数建议
- 调用方式：根据用途自动推荐，不要无意义堆参数

## 扩展技能
### 风格切换
- 用途：在不改主题的前提下切换国风/写实/电商/赛博朋克等风格
- 触发：用户说“换个风格试试”
- 调用方式：保留主体与场景，重写风格词

### 商业模板切换
- 用途：切换为电商、人像、海报、动漫、概念图模板
- 触发：用户明确商业用途
- 调用方式：直接调用对应场景模板

## 审校技能
### 审校优化
- 用途：检查手脸、构图、背景杂乱、风格冲突、参数过量等问题
- 触发：输出前或用于交付时
- 调用方式：补负面词，删冗余词，提升可执行性


---

## 三、输入/输出模板


### 案例模板.md

# 案例模板

## 示例需求
帮我写一个国风汉服人像 Prompt，用于小红书封面，3:4，画面要干净。

## 标准处理流程
1. 先调用「需求澄清 / 问题定义 / 阶段识别」类核心技能
2. 再调用主生成技能，产出首版结果
3. 如有特定商业场景，再调用扩展技能
4. 交付前调用审校技能

## 案例输出要求
- 输出要可复制、可交付、可继续修改。
- 至少给 1 个主结果和 1 个备选结果。

### 输入模板.md

# 输入模板

> 客户只要按这个模板填空，Agent 就能更快给出稳定结果。

```text
主体/对象：
场景：
风格倾向：
用途：
比例：
禁止元素：
```

## 使用建议
- 输入越具体，输出越稳定。
- 如果不确定某项，可以留空，由 Agent 先进行需求澄清。

### 输出模板.md

# 输出模板

> 标准版建议统一按下面结构输出，方便客户直接使用。

## 推荐输出结构
1. 主 Prompt
2. 保守版 Prompt
3. 风格加强版 Prompt
4. 参数建议
5. 负面提示词

## 输出原则
- 先给结论，再给补充说明。
- 能模板化就模板化。
- 能直接复制使用就不要只给概念。

---

## 四、知识库 / memory


### 参数模板.md

# 参数模板

> AI绘画提示词Agent 专用参数速查与模板

---

## 一、Midjourney 参数

### 常用参数

| 参数 | 全称 | 功能 | 示例 |
|------|------|------|------|
| --ar | --aspect | 宽高比 | --ar 16:9 |
| --s | --stylize | 风格化程度(0-1000) | --s 250 |
| --c | --chaos | 随机性(0-100) | --c 50 |
| --v | --version | 模型版本 | --v 6 |
| --iw | --image-weight | 图像提示权重(0-2) | --iw 0.5 |
| --no | --no | 排除元素 | --no people |
| --seed | --seed | 种子值 | --seed 12345 |
| --tile | --tile | 平铺图像 | --tile |
| --q | --quality | 质量(0.25-2) | --q 1 |
| --stop | --stop | 提前停止(10-100) | --stop 90 |
| --style | --style | 风格模式 | --style raw |
| --weird | --weird | 奇怪程度(0-3000) | --weird 500 |

### 宽高比参考

| 比例 | 用途 | 参数 |
|------|------|------|
| 1:1 | 社交媒体头像、方图 | --ar 1:1 |
| 4:3 | 照片、标准比例 | --ar 4:3 |
| 3:4 | 竖版人像 | --ar 3:4 |
| 16:9 | 横向视频、海报 | --ar 16:9 |
| 9:16 | 竖版视频、Story | --ar 9:16 |
| 21:9 | 电影宽屏 | --ar 21:9 |
| 2:3 | 摄影竖版 | --ar 2:3 |
| 3:2 | 摄影横版 | --ar 3:2 |

### 版本选择

| 版本 | 特点 | 适用场景 |
|------|------|----------|
| --v 1 | 最早版本 | 复古风格 |
| --v 2 | 细节增强 | 写实 |
| --v 3 | 风格范围广 | 通用 |
| --v 4 | 艺术感强 | 插画、概念 |
| --v 5 | 写实增强 | 摄影、人像 |
| --v 6 | 最新版本 | 全面提升 |
| --v 6.1 | 细节修复 | 人像最优 |
| --niji | 动漫风格 | 二次元 |

### 风格化程度 (--s)

| 值 | 效果 | 适用 |
|---|------|------|
| 0-50 | 接近描述 | 精准控制 |
| 50-200 | 平衡 | 通用 |
| 200-500 | 艺术化 | 创意 |
| 500-1000 | 高度风格化 | 抽象艺术 |

---

## 二、Stable Diffusion 参数

### 采样器

| 采样器 | 速度 | 质量 | 适用 |
|--------|------|------|------|
| Euler | 快 | 中 | 快速测试 |
| Euler a | 中 | 好 | 动漫 |
| DPM++ 2M | 快 | 好 | 通用推荐 |
| DPM++ SDE | 慢 | 最好 | 写实 |
| DDIM | 慢 | 好 | 高细节 |
| LCM | 最快 | 中 | 快速出图 |
| UniPC | 快 | 好 | 平衡 |

### 分辨率

| 模式 | 宽度 | 高度 | 适用 |
|------|------|------|------|
| 方形 | 512 | 512 | 通用测试 |
| 竖版 | 512 | 768 | 人像 |
| 横版 | 768 | 512 | 风景 |
| 宽屏 | 896 | 512 | 电影感 |
| SDXL | 1024 | 1024 | 高质量 |

### Lora 权重

| 权重 | 效果 |
|------|------|
| 0.3-0.5 | 轻微影响 |
| 0.6-0.8 | 明显风格 |
| 0.9-1.2 | 强风格 |

---

## 三、Prompt 模板

### 基础模板

```
[主体描述] --[参数]
```

示例:
```
a cute cat sitting on a couch --ar 16:9 --v 6 --s 250
```

### 完整模板

```
[主体] + [动作/姿态] + [环境] + [光照] + [时间], [媒介] + [构图] + [色彩] + [风格] --[参数]
```

示例:
```
a beautiful woman wearing a red dress, standing in a dark forest, dramatic cinematic lighting, golden hour, portrait photography, close-up, moody atmosphere, film grain --ar 3:4 --v 6 --s 300 --no blur
```

### 电商模板

```
[产品名称], [角度], [背景], [光线], [风格], commercial photography --ar 1:1 --v 6 --s 200 --q 1
```

示例:
```
perfume bottle on marble table, 45-degree angle, soft gradient background, studio lighting, minimalist, commercial photography --ar 1:1 --v 6 --s 200
```

### 人物模板

```
[性别/年龄] [描述], [表情], [服装], [姿势], [场景], [风格] --ar [比例] --v 6 --s [值]
```

示例:
```
young woman with long hair smiling, wearing casual dress, standing in garden, soft sunlight, natural look, portrait photography --ar 3:4 --v 6 --s 250
```

### 场景模板

```
[场景类型], [时间], [天气], [光照], [风格] --ar 16:9 --v 6 --s 200
```

示例:
```
futuristic city at night, rainy, neon lights, cyberpunk, cinematic lighting --ar 16:9 --v 6 --s 350
```

---

## 四、负面提示词模板

### 通用负面词

```
low quality, worst quality, blurry, extra fingers, bad hands, deformed, ugly, bad anatomy, disfigured, mutation, mutated, out of frame, poorly drawn face, poorly drawn hands, missing fingers
```

### 写实负面词

```
worst quality, low quality, normal quality, lowres, deformed, distorted, disfigured, mutation, mutated, ugly, bad anatomy, bad hands, bad proportions, wide nose, long body
```

### 动漫负面词

```
lowres, bad anatomy, bad hands, text, error, missing fingers, extra digit, fewer digits, cropped, worst quality, low quality, normal quality, jpeg artifacts, signature, watermark, username
```

### 建筑/室内负面词

```
worst quality, low quality, clutter, clutter, messy, dirty, unclear, blurry, distorted, deformed
```

---

## 五、权重语法

### Midjourney

```
cat::2 dog::1  # cat权重是dog的2倍
cat::0.5  # 降低cat权重
cat::1.5  # 提高cat权重
```

### Stable Diffusion

```
(masterpiece:1.2), (best quality:1.1), ((ultra detailed)), illustration, beautiful detailed eyes
```

---

## 六、工作流建议

### 1. 新手入门流程

1. 描述主体
2. 添加媒介风格
3. 选择构图
4. 设定光线
5. 添加1-2个风格词
6. 设置基础参数

### 2. 进阶优化流程

1. 先出基础版
2. 添加风格参考 --sref
3. 调整参数 --ar / --c
4. 添加负面提示
5. 微调权重

### 3. 批量生产流程

1. 确定风格模板
2. 保存为预设
3. 固定 --seed
4. 批量生成
5. 筛选后微调

---

## 更新日志

- 2026-03-10: 首次整合蜂群收集资料


### 参考资料.md

# AI绘画提示词Agent 参考资料库

> 本资料库用于 AI绘画提示词Agent 的提示词生成与优化。
> 所有内容均经过筛选，可直接用于提示词模板。

---

## 一、官方文档

### Midjourney 官方文档
- 链接: https://docs.midjourney.com/docs/prompts
- 核心内容: Prompt 基本语法、图像提示、参数详解、提示词权重
- 用途: 权威参考，必读

### Stable Diffusion Art Prompt Guide
- 链接: https://stable-diffusion-art.com/prompt-guide/
- 核心内容: SD prompt 语法、负面提示词、风格关键词库、采样器选择
- 用途: SD 用户专用指南

---

## 二、GitHub 优质仓库

### ⭐ 必看仓库

#### 1. willwulfken/MidJourney-Styles-and-Keywords-Reference
- Stars: 12.3k
- 链接: https://github.com/willwulfken/MidJourney-Styles-and-Keywords-Reference
- 描述: MidJourney 风格和关键词参考大全，包含分辨率对比、图像权重等
- 用途: 完整风格词库、关键词分类、参数指南

#### 2. hua1995116/awesome-ai-painting
- Stars: 11.7k
- 链接: https://github.com/hua1995116/awesome-ai-painting
- 描述: AI绘画资料合集（国内外平台、教程、参数、部署）
- 用途: Stable Diffusion 资源、AnimateDiff/SDXL Turbo、教程合集

#### 3. rockbenben/img-prompt
- Stars: 293
- 链接: https://github.com/rockbenben/img-prompt
- 描述: AI图像提示词生成器，5000+ 提示词，18种语言
- 用途: 提示词模板库，可直接复用

#### 4. soulteary/docker-prompt-generator
- Stars: 1.2k
- 链接: https://github.com/soulteary/docker-prompt-generator
- 描述: 使用模型生成作图咒语，支持 MidJourney、Stable Diffusion
- 用途: LLM 生成提示词后端服务

---

## 三、视频教程

### YouTube 推荐

| 视频 | 频道 | 播放量 | 链接 |
|------|------|--------|------|
| A Perfect Midjourney Prompt Formula | Theoretically Media | 19万 | https://www.youtube.com/watch?v=j-GZvXgfgaY |
| Ultimate Guide to Cinematic & Photorealistic AI Image Prompts | Tao Prompts | 8.5万 | https://www.youtube.com/watch?v=HWOLsh-7ZHQ |
| Prompt Engineering Tips for Midjourney | Wade McMaster | 6.5万 | https://www.youtube.com/watch?v=rg__-0WXctw |
| The ULTIMATE Beginners Guide to Midjourney in 2025 | Future Tech Pilot | 32万 | https://www.youtube.com/watch?v=vUj4VNXXC1c |

### B站 推荐

| 视频 | UP主 | 播放量 | 链接 |
|------|------|--------|------|
| 【全108集】SD+ComfyUI+Midjourney保姆级教程 | comfyui | 53.1万 | https://www.bilibili.com/video/BV15XPWe8Enu/ |
| Stable Diffusion提示词全攻略 | CG迷李辰 | 22.5万 | https://www.bilibili.com/video/BV1eP411Y7SD/ |
| 【建议收藏】5个神级AI提示词网站 | 哈利本利- | 27.3万 | https://www.bilibili.com/video/BV1as4y1w7XT/ |
| Midjourney+ChatGPT精准控制关键词 | CG迷李辰 | 14.6万 | https://www.bilibili.com/video/BV1PW4y1f7GC/ |

---

## 四、Agent Skills 推荐

### P0 强烈推荐安装

#### 1. midjourney-prompt-engineering
- SkillHub（国内优先）：打开 `https://skillhub.tencent.com/` 搜索 `midjourney-prompt-engineering` 并按页面提示安装
- 备选（有 GitHub / 可翻墙环境）：`npx skills add justinperea/midjourney-cc-skill@midjourney-prompt-engineering -g -y`
- 描述: Midjourney V7 提示词工程完整指南，含参数、风格码、学习循环
- 核心功能:
  - V7 参数文档、翻译表、失败模式诊断
  - 7维度评分系统（主体/光线/色彩/情绪/构图/材质/空间）
  - SQLite 持久化学习
  - 命令: /new-session, /log-iteration, /reflect, /discover-styles

#### 2. ai-artist
- SkillHub（国内优先）：打开 `https://skillhub.tencent.com/` 搜索 `ai-artist` 并按页面提示安装
- 备选（有 GitHub / 可翻墙环境）：`npx skills add binhmuc/autobot-review@ai-artist -g -y`
- 描述: 跨模型提示词工程：LLM + 图像生成 + 视频生成
- 核心功能:
  - 覆盖 Midjourney / DALL-E / Stable Diffusion / Flux / Imagen / Veo
  - 提示词结构模板：主体→风格→构图→质量→负面
  - 模型特定语法速查表

### P1 推荐

#### 3. stable-diffusion-image-generation
- SkillHub（国内优先）：打开 `https://skillhub.tencent.com/` 搜索 `stable-diffusion-image-generation` 并按页面提示安装
- 备选（有 GitHub / 可翻墙环境）：`npx skills add davila7/claude-code-templates@stable-diffusion-image-generation -g -y`
- 描述: HuggingFace Diffusers 库进行 Stable Diffusion 图像生成
- 核心功能: Python 代码级指南、SD 1.5/SDXL/SD 3.0/Flux 多模型支持

---

## 五、Prompt 结构模板

### 核心公式

```
[主体描述] + [动作/姿态] + [环境/场景] + [光照] + [时间], [媒介] + [构图] + [色彩] + [风格] --参数
```

### 详细模板

```
[主体] + [媒介] + [构图] + [场景] + [风格]
```

### 要素优先级

1. **具体** - 越具体越精准 (如 "golden retriever" > "dog")
2. **顺序** - 重要元素放前面
3. **风格词** - 添加艺术家/风格名称增强效果
4. **参数** - 适当使用 --ar, --s 等调整输出
5. **负面提示** - 用 --no 排除不需要的元素

### 权重语法

- `cat::2 dog` - cat 权重是 dog 的 2 倍
- `--iw 0.5` - 图像提示权重
- `--seed` - 复现相似结果

---

## 六、参数速查表

| 参数 | 功能 | 示例 |
|------|------|------|
| --ar | 宽高比 | --ar 16:9 |
| --stylize / --s | 风格化程度 | --s 250 |
| --chaos / --c | 随机性 | --c 50 |
| --no | 排除元素 | --no people |
| --iw | 图像提示权重 | --iw 0.5 |
| --seed | 种子值 | --seed 12345 |
| --tile | 平铺 | --tile |
| --v | 版本 | --v 6 |
| --style raw | 原始输出 | --style raw |

---

## 七、风格关键词库

### 媒介类型
- 油画 (oil painting)
- 水彩画 (watercolor)
- 摄影 (photograph)
- 3D渲染 (3D render)
- 素描 (sketch)
- 版画 (printmaking)
- 中国画 (Chinese ink painting)

### 光线
- 自然光 (natural lighting)
- 电影光 (cinematic lighting)
- 舞台光 (stage lighting)
- 柔光 (soft lighting)
- 轮廓光 (rim lighting)
- 体积光 (volumetric lighting)

### 风格
- 赛博朋克 (cyberpunk)
- 蒸汽朋克 (steampunk)
- 极简主义 (minimalist)
- 巴洛克 (baroque)
- 浮世绘 (ukiyo-e)
- 包豪斯 (bauhaus)

### 艺术家
- 梵高 (Van Gogh)
- 毕加索 (Picasso)
- 莫奈 (Monet)
- 达芬奇 (Da Vinci)
- 葛饰北斋 (Hokusai)

---

## 八、负面提示词模板

### 通用
```
low quality, blurry, extra fingers, bad hands, deformed, ugly, bad anatomy, disfigured, mutation, mutated
```

### 写实
```
worst quality, low quality, normal quality, lowres, деформированные руки, деформированные пальцы, деформированное лицо
```

### 动漫/插画
```
lowres, bad anatomy, bad hands, text, error, missing fingers, extra digit, fewer digits, cropped, worst quality, low quality
```

---

## 九、整合建议

### 国内优先安装（SkillHub）

1. 打开：`https://skillhub.tencent.com/`
2. 如果尚未安装 SkillHub 商店，先按这个说明安装：
   `https://skillhub-1388575217.cos.ap-guangzhou.myqcloud.com/install/skillhub.md`
3. 在 SkillHub 搜索并安装（按优先级）：
   - `midjourney-prompt-engineering`
   - `ai-artist`
   - `stable-diffusion-image-generation`（可选）

### 备选（有 GitHub / 可翻墙环境才用）

```bash
# 推荐安装
npx skills add justinperea/midjourney-cc-skill@midjourney-prompt-engineering -g -y
npx skills add binhmuc/autobot-review@ai-artist -g -y
# 可选
npx skills add davila7/claude-code-templates@stable-diffusion-image-generation -g -y
```

### 资料优先级

1. **必读**: Midjourney 官方文档 + Prompt 结构模板
2. **必看**: willwulfken/MidJourney-Styles-and-Keywords-Reference
3. **必装**: midjourney-prompt-engineering skill
4. **进阶**: ai-artist skill + 风格关键词库

---

## 更新日志

- 2026-03-10: 首次整合蜂群收集资料
  - 来源: Web搜索 + GitHub + YouTube/B站 + Skills搜索 + Reddit
  - 新增: 5个高质量仓库 + 10+视频教程 + 3个Agent Skills


### 风格库.md

# 风格库

> AI绘画提示词Agent 专用风格关键词库

---

## 一、媒介风格

### 绘画类型
| 中文 | 英文 | 适用场景 |
|------|------|----------|
| 油画 | oil painting | 艺术感、厚重感 |
| 水彩画 | watercolor | 清新、透明感 |
| 丙烯画 | acrylic painting | 鲜艳、现代感 |
| 素描 | sketch / pencil drawing | 简约、线条感 |
| 版画 | printmaking / woodblock | 复古、纹理感 |
| 中国画 | Chinese ink painting / shuimohua | 国风、意境 |
| 日本画 | Nihonga | 和风、精致 |
| 壁画 | mural / fresco | 古老、宏大 |

### 摄影类型
| 中文 | 英文 | 适用场景 |
|------|------|----------|
| 肖像摄影 | portrait photography | 人像、质感 |
| 风景摄影 | landscape photography | 自然、宏观 |
| 街拍 | street photography | 都市、纪实 |
| 微距摄影 | macro photography | 细节、昆虫 |
| 时尚摄影 | fashion photography | 服装、杂志 |
| 产品摄影 | product photography | 电商、广告 |

### 数字艺术
| 中文 | 英文 | 适用场景 |
|------|------|----------|
| 3D渲染 | 3D render / CGI | 立体、质感 |
| 概念艺术 | concept art | 设计、幻想 |
| 像素艺术 | pixel art | 游戏、复古 |
| 矢量插画 | vector illustration | 扁平、现代 |
| 扁平化设计 | flat design | UI、简洁 |

---

## 二、光线风格

### 自然光
| 中文 | 英文 | 效果 |
|------|------|------|
| 日落 | sunset / golden hour | 暖色调、逆光 |
| 日出 | sunrise / dawn | 柔和、渐变 |
| 正午阳光 | midday sun | 强烈、硬阴影 |
| 月光 | moonlight | 冷色调、神秘 |
| 星光 | starlight | 夜晚、梦幻 |

### 人造光
| 中文 | 英文 | 效果 |
|------|------|------|
| 电影光 | cinematic lighting | 戏剧性、层次 |
| 舞台光 | stage lighting | 聚焦、表演感 |
| 霓虹灯 | neon lights | 赛博、夜景 |
| 演播室光 | studio lighting | 专业、均匀 |
| 烛光 | candlelight | 温暖、柔和 |

### 特殊光效
| 中文 | 英文 | 效果 |
|------|------|------|
| 体积光 | volumetric lighting | 空气感、丁达尔 |
| 轮廓光 | rim lighting / backlight | 边缘发光、分离主体 |
| 柔光 | soft lighting | 柔和、梦幻 |
| 硬光 | hard lighting | 锐利、戏剧 |
| 光晕 | lens flare | 真实感、太阳 |

---

## 三、构图风格

### 视角
| 中文 | 英文 | 适用 |
|------|------|------|
| 正面 | front view | 肖像、对称 |
| 侧面 | side view | 轮廓、剪影 |
| 45度角 | 45-degree angle | 立体感 |
| 俯视 | overhead view / top-down | 顶部物体 |
| 仰视 | low angle / worm's-eye | 宏伟、压迫 |
| 鸟瞰 | bird's eye view | 宏观、地图 |
| 特写 | close-up | 细节、表情 |

### 景别
| 中文 | 英文 | 适用 |
|------|------|------|
| 远景 | long shot / wide shot | 环境、氛围 |
| 全景 | full shot | 完整人物 |
| 中景 | medium shot | 半身 |
| 近景 | close-up | 表情、细节 |
| 特写 | extreme close-up | 眼睛、局部 |

### 构图方式
| 中文 | 英文 | 效果 |
|------|------|------|
| 三分法 | rule of thirds | 平衡、协调 |
| 对称 | symmetry | 正式、平衡 |
| 对角线 | diagonal | 动感、紧张 |
| 引导线 | leading lines | 引导视线 |
| 框架 | framing | 聚焦、层次 |
| 留白 | negative space | 简约、呼吸感 |

---

## 四、艺术家风格

### 古典大师
| 艺术家 | 风格特点 | 提示词 |
|--------|----------|--------|
| 梵高 Van Gogh | 后印象派、旋涡笔触、浓烈色彩 | Van Gogh style, post-impressionist, swirling brushstrokes |
| 莫奈 Monet | 印象派、模糊光影、渐变 | Monet style, impressionist, soft light, blurred edges |
| 毕加索 Picasso | 立体主义、几何分解、抽象 | Picasso style, cubist, geometric, abstract |
| 达芬奇 Da Vinci | 文艺复兴、细腻写实 | Da Vinci style, renaissance, sfumato |
| 维米尔 Vermeer | 荷兰黄金时代、静谧光影 | Vermeer style, dutch golden age, chiaroscuro |

### 现代艺术家
| 艺术家 | 风格特点 | 提示词 |
|--------|----------|--------|
| 葛饰北斋 Hokusai | 浮世绘、波浪、富士山 | Hokusai style, ukiyo-e, wave pattern |
| 蒙德里安 Mondrian | 几何抽象、红黄蓝 | Mondrian style, geometric abstraction, primary colors |
| 草间弥生 Yayoi Kusama | 波点、无限重复 | Yayoi Kusama style, polka dots, infinite |
| 村上隆 Takashi Murakami | 超扁平、卡通 | Takashi Murakami style, superflat, anime |

### 当代数字
| 风格 | 特点 | 提示词 |
|------|------|--------|
| 赛博朋克 | 霓虹、雨夜、亚洲城市 | cyberpunk, neon, rainy city, asian fusion |
| 蒸汽朋克 | 机械、维多利亚、齿轮 | steampunk, victorian, brass machinery |
| 极简主义 | 干净、留白、几何 | minimalist, clean lines, white space |
| 孟菲斯风格 | 色彩爆炸、几何图案 | memphis design, colorful patterns, 1980s |

---

## 五、情绪氛围

| 情绪 | 英文 | 适用风格 |
|------|------|----------|
| 神秘 | mysterious / enigmatic | 暗调、轮廓光 |
| 浪漫 | romantic / dreamy | 柔光、暖调 |
| 恐怖 | horror / eerie | 暗调、血色、扭曲 |
| 欢乐 | joyful / festive | 明亮、饱和色彩 |
| 悲伤 | melancholic / sorrowful | 冷调、雨水、孤独 |
| 平静 | peaceful / serene | 柔和、自然光 |
| 紧张 | tense / suspenseful | 暗角、动态模糊 |
| 怀旧 | nostalgic / vintage | 泛黄、颗粒、复古 |

---

## 六、场景风格

### 室内
| 场景 | 英文 | 风格关键词 |
|------|------|------------|
| 极简客厅 | minimalist living room | 白墙、木地板、自然光 |
| 工业风 | industrial loft | 砖墙、金属管道、暗调 |
| 和室 | japanese room | 榻榻米、移门、柔和 |
| 温室 | greenhouse | 植物、玻璃、阳光 |

### 室外
| 场景 | 英文 | 风格关键词 |
|------|------|------------|
| 都市夜景 | urban night | 霓虹、车流、雨 |
| 乡村田园 | countryside | 田野、蓝天、质朴 |
| 海岸日落 | coastal sunset | 沙滩、海浪、金色 |
| 森林迷雾 | misty forest | 树木、雾气、神秘 |

---

## 使用建议

1. **组合使用**: 媒介 + 光线 + 构图 + 风格 = 完整Prompt
2. **权重调整**: 重要风格放前面，或使用 `::` 调整权重
3. **负面提示**: 根据风格添加对应的负面词
4. **参数配合**: 风格化用 `--s`，版本用 `--v`

---

## 更新日志

- 2026-03-10: 首次整合蜂群收集资料


---

## 五、使用说明

1. 把本文件完整内容交给客户。
2. 客户将其中适合作为系统提示词/Agent 说明的部分导入到自己的 Agent。
3. 同文件内的模板、FAQ、案例库、技能说明可作为该 Agent 的长期知识库。
4. 如果客户需要更轻量版本，可只保留『资料包总览』与『内置技能』部分。

## 六、版本定位

- 当前文件：单文件完整包
- 可用于开源引流 / 标准版交付 / 定制前样例
