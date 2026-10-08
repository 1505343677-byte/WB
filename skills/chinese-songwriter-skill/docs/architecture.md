# Skill 架构说明

`chinese-songwriter-skill` 采用分层架构，把中文歌曲创作拆解为需求理解、歌词创作、审核优化、演唱设计和 Suno 生成五个协作层。这样可以让 AI 不只是“写几段歌词”，而是按照真实音乐创作流程交付一套完整歌曲方案。

## 总体流程

```text
用户需求
  ↓
需求理解层
  ↓
歌词创作层
  ↓
审核层
  ↓
演唱设计层
  ↓
Suno 生成层
  ↓
完整歌曲创作方案
```

## 1. 需求理解层

目标：

- 理解用户想创作什么歌。
- 判断歌曲用途、主题、人物、场景、情绪和目标听众。
- 识别演唱形式：男声独唱、女声独唱、男女对唱或合唱。
- 判断是否需要读取特定模板或知识文件。

对应资源：

- `SKILL.md`
- `templates/`
- `knowledge/music_style_library.md`

输出重点：

- 创作目的
- 歌曲类型
- 情绪方向
- 歌曲定位
- 副歌核心表达

## 2. 歌词创作层

目标：

- 根据主题、故事和情绪生成完整中文歌词。
- 保证中文自然表达、具体画面、情绪递进和可演唱性。
- 避免 AI 套路化表达、空泛口号和不可唱的散文化句子。

对应资源：

- `prompts/lyric_creator.md`
- `knowledge/song_structure.md`
- `knowledge/lyric_rules.md`
- `knowledge/rhyme_library.md`

输出重点：

- 歌曲名称
- 歌曲定位
- 创作前分析
- 完整歌词
- 副歌核心记忆点

## 3. 审核层

目标：

- 从专业音乐制作和歌词策划角度审核歌词。
- 检查文学性、情绪、演唱性、原创性和传播性。
- 发现模板化、强行押韵、情绪重复和副歌不抓耳等问题。
- 给出可执行修改建议和优化版本。

对应资源：

- `prompts/lyric_reviewer.md`
- `knowledge/lyric_rules.md`

输出重点：

- 评分
- 问题
- 修改建议
- 优化版本

## 4. 演唱设计层

目标：

- 根据歌曲主题和歌词设计最适合的演唱形式。
- 为男声独唱、女声独唱和男女对唱分别设计声音特点、情绪表达和歌词分配。
- 对男女对唱场景明确双方角色、情绪关系和合唱高潮。

对应资源：

- `prompts/duet_designer.md`
- `templates/`

输出重点：

- 演唱形式
- 角色设定
- 演唱建议
- 歌词分配方案

## 5. Suno 生成层

目标：

- 将歌曲定位、歌词情绪和演唱形式转化为可直接复制到 Suno 的英文 Style Prompt。
- 输出 Negative Prompt，减少人工感人声、过度 Auto-Tune、混乱编曲和不自然旋律。
- 提供中文制作说明，帮助用户理解音乐类型、速度、乐器、演唱方向和情绪。

对应资源：

- `prompts/suno_prompt_generator.md`
- `knowledge/music_style_library.md`

输出重点：

- English Style Prompt
- Negative Prompt
- 中文制作说明

## 质量控制

每次完整创作都应通过以下检查：

- 歌词是否有具体画面，而不是抽象情绪堆叠。
- 副歌是否有一句清晰可记的核心表达。
- 情绪是否从主歌到副歌、桥段有推进。
- 演唱设计是否匹配男声、女声或男女对唱。
- Suno Prompt 是否包含 Genre、Mood、Vocal、Instrumentation、Arrangement、Production。
- 是否避免模仿具体歌手、词人或现有歌曲的标志性表达。

## 可扩展方向

- 增加更多细分风格模板，例如 R&B、说唱、儿童歌曲、广告歌。
- 增加更细的韵脚库和副歌 Hook 写法库。
- 增加不同 AI 音乐平台的 Prompt 适配层。
- 增加更多测试案例和完整 Demo，用于评估输出稳定性。
