# 网络来源与适用边界

查阅日期：2026-10-15。以下为搜索后选用的官方文档或作者一手经验，并非完整文献综述。正文是短转述与独立整理的工作流，没有复制完整指南。stable/master 与平台规则可能变化；实施前按项目版本复查。

| 来源 | 采用要点 | 范围与查阅状态 |
|---|---|---|
| [Derek Yu — Finishing a Game](https://makegames.tumblr.com/post/1136623767/finishing-a-game) | 原型、核心、收敛、完成成本 | 正文已读取；作者经验，不保证项目成功 |
| [Harry Florencio — Pre-Production](https://www.gamedeveloper.com/game-platforms/what-you-should-take-out-of-pre-production) | 时间约束、切片、管线、交接验收 | 正文已读取；作者制作经验，阶段术语自行定义 |
| [Godot — Scene organization](https://docs.godotengine.org/en/stable/tutorials/best_practices/scene_organization.html) | 显式依赖、聚焦职责、入口与世界/UI | 正文已读取；生命周期不跨引擎照搬 |
| [Godot — Project organization](https://docs.godotengine.org/en/stable/tutorials/best_practices/project_organization.html) | 关联资源就近组织、命名和大小写 | 正文已读取；导入和元数据规则依引擎 |
| [Godot — Size and anchors](https://docs.godotengine.org/en/stable/tutorials/ui/size_and_anchors.html) | 视口变化下的锚点布局 | 正文已读取；API 需匹配版本 |
| [Game Accessibility Guidelines — Full list](https://gameaccessibilityguidelines.com/full-list/) | 可读性、输入与访问性检查入口 | 首次打开成功，后续定位失败，细节从专题复查 |
| [Game Accessibility Guidelines — Contrast](https://gameaccessibilityguidelines.com/provide-high-contrast-between-text-ui-and-background/) | 动态背景对比与约 4.5:1 参考 | 专题正文由搜索返回；不能证明整体游戏可访问性 |
| [Valve — Character Art Guide](https://help.steampowered.com/en/faqs/view/0688-7692-4D5A-1935) | 轮廓辨识、明度与焦点 | 官方搜索摘要可核实，正文抓取受限；只采用这些原则，不推广 Dota 英雄约束 |
| [Unity — 2D art style reference](https://docs.unity.com/en-us/engine/6000.5/manual/unity2d/2d-game-development/2d-game-art-syle-reference) | 2D 表现类别与取舍入口 | 页面已打开；特定版本路径不代表其他版本支持 |
| [inkle — Writing with ink](https://github.com/inkle/ink/blob/master/Documentation/WritingWithInk.md) | 节点、选项、跳转、条件与变量 | 相关正文已读取；不自动解决运行时集成/存档 |
| [Godot — Internationalizing games](https://docs.godotengine.org/en/stable/tutorials/i18n/internationalizing_games.html) | 翻译键、上下文、占位符、复数和字体 | 正文已读取；含不同年代术语，不直接复制 API 示例 |
| [Steamworks — Localization](https://partner.steamgames.com/doc/store/localization?l=english) | 商店/游戏支持分开，按容量安排语言 | 正文已读取；后台位置、语言数量等不固化 |

容量公式、任务字段、目录示例、UI 状态表、风格页、文本字段和发布清单，是组合形成的实践模板，不是任何一个来源的完整标准，也不存在通用最佳取值。

检索但未采纳为实质依据：[Robert Nystrom — Architecture, Performance, and Games](https://gameprogrammingpatterns.com/architecture-performance-and-games.html)，搜索可见而正文两次读取失败。引用具体论点前重新读取，不把本 skill 的架构建议反向归于该书。

后续引擎实现和平台规范先查对应官方版本，记录适用范围。第三方教程可以作案例，不能替代官方 API/平台要求；不可访问页面不得标为完整核实。
