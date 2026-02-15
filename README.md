# script-shot-prompter

这个仓库用于存放基于 Trae 的自定义技能，目前包含一个将剧本文本转换为「连贯镜头提示词」的技能：`script-shot-prompter`。

## 仓库结构

- `.trae/skills/script-shot-prompter/SKILL.md`  
  该文件定义了技能的名称、描述、使用场景、输入输出格式和示例。
- `narrative_to_visual_reasoning_skill_p_0_p_1_p_2.md`  
  额外的叙事到视觉推理说明文档（如有）。

核心技能文档位置：  
[SKILL.md](file:///Users/mazhuohan/Documents/trae_projects/skills/.trae/skills/script-shot-prompter/SKILL.md)

## script-shot-prompter 做什么

- 将剧本或片段拆解为一系列镜头
- 为每个镜头生成结构化信息：镜头类型、视角、运动、主体动作与情绪、环境与光线、风格等
- 同时生成一行可直接用于 AI 文生图 / 文生视频的提示词
- 注重镜头之间的连续性（人物位置、视线方向、动作延续、光线与色调连贯）

详细的使用规则与示例见上方 SKILL.md。

## 在其他项目中使用本技能

1. 在目标项目根目录下创建目录结构（如不存在）：
   - `.trae/skills/script-shot-prompter/`
2. 将本仓库中的  
   `.trae/skills/script-shot-prompter/SKILL.md`  
   拷贝到目标项目对应目录下。
3. 在目标项目中提交并推送改动，使 Trae 能识别该技能。

之后，当你在该项目中提供剧本文本并说明希望生成「分镜 / 镜头提示词」时，Trae 会根据此技能的定义来工作。

## 扩展更多技能

如果你想继续为该仓库添加其他技能：

1. 在 `.trae/skills/` 下创建新的技能目录，如：`my-new-skill/`
2. 在目录中编写对应的 `SKILL.md`，包含：
   - frontmatter：`name`、`description`
   - 技能目的、触发时机、输入输出规范、注意事项与示例
3. 提交并推送到 GitHub，Trae 即可在需要时调用新的技能。
