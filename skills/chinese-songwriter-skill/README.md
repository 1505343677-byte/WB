# 中文歌曲创作 Skill

> AI 时代的中文音乐创作工具：从一句主题出发，生成可演唱歌词、演唱设计、歌词优化建议和 Suno AI 音乐 Prompt。

![Skill Type](https://img.shields.io/badge/Skill-AI%20Songwriting-blue)
![Language](https://img.shields.io/badge/Language-Chinese-red)
![AI Powered](https://img.shields.io/badge/AI-Powered-purple)
![Open Source](https://img.shields.io/badge/Open%20Source-Yes-green)

一个面向 AI Agent 的专业中文歌曲创作 Skill，用于生成中文歌词、男女演唱设计、歌词优化方案，以及可直接用于 Suno AI 的英文音乐 Prompt。

它把华语歌词创作、音乐制作思路和 AI 生成工作流整理成一套可复用的 Skill 配置，帮助创作者在 AI 时代更稳定地完成中文歌曲 Demo、主题曲、企业歌、公益歌和影视 OST 构思。

## 项目简介

`chinese-songwriter-skill` 不是简单的歌词生成提示词，而是一套面向真实音乐创作流程设计的 AI Skill。它把需求理解、歌曲定位、歌词创作、歌词审核、演唱形式设计和 Suno Prompt 生成拆成可复用模块，让 AI 输出更稳定、更专业、更接近可制作 Demo。

## 核心能力

- 🎼 歌词创作：根据主题、故事、情绪和场景生成可演唱中文歌词。
- 🎙️ 男女演唱设计：支持男声独唱、女声独唱、男女对唱和合唱分配。
- 🎛️ Suno Prompt 生成：输出英文 Style Prompt、Negative Prompt 和中文制作说明。
- ✍️ 歌词优化：从文学性、情绪、演唱性、原创性和传播性审核并改写歌词。

## 使用流程

```text
输入主题
  ↓
AI 分析创作目的、歌曲类型、情绪方向和演唱形式
  ↓
生成歌曲定位、副歌核心表达和完整歌词
  ↓
生成演唱方案、编曲方向和 Suno AI 音乐 Prompt
```

典型输出包含：

1. 创作理解
2. 歌曲定位
3. 副歌核心表达
4. 完整歌词
5. 演唱与编曲方案
6. Suno Style Prompt
7. 歌词自检

## 使用案例

你可以这样提出需求：

```text
请写一首关于异地恋重逢的中文流行歌。
要求：女声独唱，情绪温柔但副歌要有爆发。
歌词里要有机场、凌晨和没删掉的聊天记录。
最后生成 Suno Prompt。
```

也可以用于更具体的商业或内容场景：

```text
为一家新能源制造企业写十周年宣传歌。
要求：大气、有团队感，不官腔，适合发布会男女领唱加合唱。
```

完整 Demo 请查看：

- [examples/quick_start.md](examples/quick_start.md)：快速调用示例
- [examples/demo_cases.md](examples/demo_cases.md)：5 个完整歌曲创作案例
- [tests/test_cases.md](tests/test_cases.md)：15 个真实测试场景

## 示例截图

> 这里预留项目截图位置。  
> 建议放置 AI 输出完整歌曲方案、Suno Prompt 生成结果、歌词审核优化结果等截图。

```text
docs/images/demo-output.png
docs/images/suno-prompt.png
docs/images/lyric-review.png
```

## 安装方式

将本仓库放入支持 Skill 加载的目录中，例如：

```text
chinese-songwriter-skill/
├── SKILL.md
├── prompts/
├── knowledge/
├── templates/
├── examples/
└── tests/
```

在 Codex 或其他支持 Skill 的 AI Agent 环境中启用该目录后，即可通过自然语言调用中文歌曲创作能力。

## 使用方法

### 1. 直接创作歌曲

```text
请根据“成年人终于学会告别”写一首男声独唱流行歌。
要求有城市夜晚的画面，副歌要有记忆点，并生成 Suno Prompt。
```

### 2. 审核和优化歌词

```text
请审核下面这首歌词，从文学性、情绪、演唱性、原创性和传播性评分，并给出优化版本。
```

### 3. 设计男女对唱

```text
主题是分手后的最后一通电话。
请设计男女对唱方案，包括男声角色、女声角色、双方情绪关系和合唱高潮。
```

### 4. 生成 Suno Prompt

```text
根据这首歌的定位和歌词，生成适合 Suno 的英文 Style Prompt、Negative Prompt 和中文制作说明。
```

## 项目结构

```text
.
├── SKILL.md
├── README.md
├── LICENSE
├── docs/
│   ├── architecture.md
│   └── images/
│       └── README.md
├── prompts/
│   ├── lyric_creator.md
│   ├── lyric_reviewer.md
│   ├── duet_designer.md
│   └── suno_prompt_generator.md
├── knowledge/
│   ├── song_structure.md
│   ├── lyric_rules.md
│   ├── rhyme_library.md
│   └── music_style_library.md
├── templates/
│   ├── love_song.md
│   ├── youth_song.md
│   ├── enterprise_song.md
│   ├── public_welfare_song.md
│   └── cinematic_song.md
├── examples/
│   ├── quick_start.md
│   └── demo_cases.md
└── tests/
    └── test_cases.md
```

## 适用场景

- 爱情歌曲：暗恋、热恋、异地恋、失恋、重逢、婚礼告白。
- 青春校园：毕业、同桌、初恋、友情、成长和回忆。
- 商业音乐：企业宣传歌、品牌主题歌、发布会主题曲。
- 公益歌曲：教育、环保、儿童、乡村、社会互助。
- 影视 OST：人物主题曲、片尾曲、插曲、宿命感情歌。
- AI 音乐生成：为 Suno 等平台准备歌词结构和英文音乐提示词。

## 架构说明

项目采用分层 Skill 架构，包括需求理解层、歌词创作层、审核层、演唱设计层和 Suno 生成层。完整说明见 [docs/architecture.md](docs/architecture.md)。

## 未来规划

- 增加更多歌曲类型模板，如国风、R&B、说唱、儿童歌曲和广告歌。
- 补充更细分的中文韵脚库和副歌 Hook 写法。
- 增加 Suno、Udio 等 AI 音乐平台的 Prompt 适配建议。
- 建立歌词修改前后对照案例，提升审核和优化能力。
- 扩展测试案例，覆盖更多真实音乐创作需求。
- 增加截图、演示视频和发布级 Demo 输出样例。

## 开源协议

本项目使用 [MIT License](LICENSE) 开源。

## 说明

本项目不包含代码程序，是一个 AI Skill 配置项目。它通过结构化提示词、知识参考、创作模板、完整示例和测试案例，帮助 AI 更稳定地完成专业中文歌曲创作任务。
