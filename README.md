# Indie Game Development Skill

`indie-game-dev` is a Codex Skill for planning, building, and improving independent games. It is designed for solo developers and small teams working on 2D or 3D projects. The Skill helps turn an idea or a specific implementation request into a manageable piece of work, while keeping the developer's creative direction and project constraints at the center of each decision.

The Skill is useful at several stages: when a project is still an idea, when a playable prototype needs to prove its central mechanic, when an existing project needs a focused improvement, and when a build needs a more deliberate testing or release checklist. It can help with planning and review as well as implementation tasks. It does not require every project to produce a complete design document or adopt a large technical framework.

## What it helps with

### Project scope and production planning

The Skill helps define the player, target platform, core experience, gameplay loop, production constraints, and the smallest build that can test the most important assumption. It can separate essential features from optional ideas and explicit non-goals, then turn the chosen scope into milestones with observable completion conditions.

Estimates should reflect the actual team, available time, dependencies, and uncertainty. When there is little production history, estimates should be presented as ranges with assumptions rather than as precise promises. After a prototype or representative slice exists, the remaining work can be estimated using what the team has learned about its real content and integration speed.

### Project architecture and implementation

For an existing project, the Skill first looks at its documentation, folders, entry points, build configuration, and relevant code. It then recommends changes that fit the engine, engine version, project size, and current needs. Advice may cover module responsibilities, data ownership, runtime states, communication between systems, content definitions, save data, and the order in which changes can be made safely.

The goal is to keep the architecture understandable and easy to change. Direct references or a small state machine may be enough for a prototype. More involved patterns should be introduced when the project has a concrete need for them, with their maintenance cost explained. Engine-specific APIs and lifecycle details should be checked against the version the project actually uses.

### Player experience, interface, and input

The Skill helps design clear player flows and interface responsibilities. A typical project may have a main menu, gameplay interface, pause menu, and settings screen, with additional screens such as results or save selection when the game needs them. It should be clear how players move between these states, where each action returns, and which screen owns input at a given moment.

Settings should show the controls and key bindings supported by the project. In-game prompts should reflect the active binding and update when the input device or mapping changes. Menus should provide understandable focus, navigation, cancellation, and feedback for keyboard, controller, or touch input as appropriate for the target platform.

The Skill also encourages readable layouts, visible interaction states, sensible feedback, and checks for different screen sizes, aspect ratios, text lengths, and input methods. Accessibility options should match the project's audience, platform, and production capacity; the Skill should not claim that features are implemented when they are not.

### Teaching gameplay through the game

Players should be able to learn the game's goals and actions through a suitable combination of safe practice, level design, visual cues, sound, and feedback. The amount of explicit instruction depends on the genre and audience. Short prompts may still be useful, but unnecessary blocks of text should not be added to the gameplay screen or obscure important visual information.

The Skill can help plan a first-play experience and identify what to observe during a playtest: where players pause, what they misunderstand, which actions they try, and whether the game communicates the result. A team should distinguish a genuine comprehension problem from a difference in player preference, and should not claim that onboarding works simply because the developers already know how to play.

### Art direction, writing, and localization

The Skill can turn broad visual goals into a practical style guide with references, shape language, color roles, camera and composition notes, asset specifications, and an import workflow. A representative in-game view is more useful than a concept image alone because it can reveal problems with movement, occlusion, effects, and readability.

For text and narrative work, the Skill can help maintain terminology, character voice, state and branch consistency, and importable content formats. It should preserve the author's intended meaning and clearly separate proposed story changes from copy editing. Localization planning can account for placeholders, font coverage, line wrapping, language-specific text expansion, subtitles, and the difference between a translated store page and an actually localized game.

### Tutorial discovery and code migration analysis

When a developer describes an effect they want to create, the Skill can search for relevant tutorials on Bilibili and YouTube, prioritizing the project's engine and version. Where accessible, it checks video descriptions and comments for GitHub links and reports the tutorial, repository, where the link appeared, and what has been verified. If a description or comment thread cannot be inspected, the limitation should be stated instead of guessing.

The developer reviews the candidate projects and chooses one to investigate. Only then does the Skill compare the selected source with the user's project: the code responsible for the effect, engine and version compatibility, dependencies, assets, architectural coupling, migration effort, license terms, and a practical verification plan. It can recommend direct reuse, adaptation, or avoiding the migration, with evidence and uncertainty stated. It should not change the user's game project until the developer asks for implementation.

### Math concepts as game mechanics

The Skill can help developers explore how mathematical ideas might become player actions, rules, visualizations, or challenges. For example, a function curve could define a level's terrain. A player might adjust a parameter and observe how the curve changes the route through an obstacle. The mathematical relationship then affects the player's choices instead of appearing only as a formula on screen.

Other possibilities could involve geometric construction, transformations, probability, optimization, or discrete structures, depending on the intended learning goal and game genre. These are design directions, not claims that a finished educational game is included in this repository. The developer remains responsible for checking the mathematics, choosing suitable explanations and difficulty, and confirming that the mechanic teaches the intended concept rather than merely decorating the screen with notation.

## A typical working process

The Skill adapts its process to the request, but a focused task often follows this pattern:

1. **Understand the context.** Identify the intended player experience, target platform and inputs, engine and version, project stage, team capacity, and any existing implementation that matters.
2. **Choose the relevant scope.** Decide whether the task needs a short plan, a design artifact, code changes, a focused review, or a playtest and release checklist. Read only the reference material that applies.
3. **Make the work concrete.** Break a broad goal into small decisions or implementation steps with dependencies and observable outcomes. Mark assumptions and open questions.
4. **Implement or analyze in context.** Preserve the user's project, style, and chosen tools. For reference-based migrations, wait for the user's chosen source project before recommending a concrete migration path.
5. **Verify what can be verified.** Use the actual project and target setup where available. Report whether evidence came from reading the code, a static check, an engine build, runtime execution, or player testing.
6. **Hand off the next useful action.** Summarize the result, remaining risks, and the smallest meaningful next check without expanding the task into unrelated work.

## Principles that guide its recommendations

- **Start from the player's experience.** A feature is useful when it supports the intended play experience and can be verified in the game.
- **Keep scope proportional to the team.** Count the production, integration, testing, and localization cost of additional content and platforms.
- **Prefer evidence to claims.** Separate verified behavior, planned checks, and creative preference.
- **Fit the existing project.** Inspect before restructuring; solve current or near-term problems before adding abstractions.
- **Keep screens and input understandable.** Make interface hierarchy, navigation, control display, and feedback consistent with the actual game.
- **Preserve authorship.** Treat the developer's engine, visual style, game concept, and creative choices as constraints to respect, not defaults to replace.
- **Be clear about limitations.** If the engine cannot be run, distinguish code inspection from actual gameplay verification. If a link, license, version detail, or platform rule cannot be confirmed, say so.
- **Check changing technical facts.** Engine APIs, platform requirements, pricing, and license terms may change; verify the current official source when they affect an implementation or release decision.

## Repository structure

```text
skills/indie-game-dev/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── architecture.md
    ├── art-direction.md
    ├── production.md
    ├── sources.md
    ├── testing-release.md
    ├── text-narrative.md
    └── ui-ux.md
```

`SKILL.md` is the entry point. It describes when the Skill applies, how it routes work to supporting references, and the core decision constraints. The reference files hold more detailed guidance for specific tasks so that unrelated material does not need to be loaded for every request. `agents/openai.yaml` supplies the Skill's Codex-facing display name and starter prompt.

## Installation and use

Copy the complete `skills/indie-game-dev/` directory into a Codex skills directory, such as `~/.codex/skills/indie-game-dev/`. Keep `SKILL.md`, `agents/`, and `references/` together so the links from the entry point continue to resolve.

Once installed, invoke it in Codex with `$indie-game-dev`, then describe the current game task and relevant context. For example:

> Use `$indie-game-dev` to help me prototype a function-based platforming level in my existing Godot project. First inspect the project and propose the smallest playable experiment; do not restructure unrelated systems.

The example is only a prompt pattern. Engine, genre, scope, and implementation choices should come from the developer's actual project and goals.

## References

- [Production planning](skills/indie-game-dev/references/production.md) covers project briefs, scope, milestones, workload ranges, dependencies, and how to respond to schedule pressure.
- [Architecture](skills/indie-game-dev/references/architecture.md) covers player-facing interface and input conventions, module boundaries, data ownership, runtime states, saves, and implementation order.
- [UI and UX](skills/indie-game-dev/references/ui-ux.md) covers player flows, screen states, layout, controls, readability, accessibility checks, and acceptance scenarios.
- [Art direction](skills/indie-game-dev/references/art-direction.md) covers visual exploration, style sheets, asset pipelines, production budgets, and in-game visual review.
- [Text and narrative](skills/indie-game-dev/references/text-narrative.md) covers editing, branching content, import formats, voice and terminology, and localization checks.
- [Testing and release](skills/indie-game-dev/references/testing-release.md) covers playtest questions, issue records, regression paths, candidate builds, and release preparation.
- [Sources and boundaries](skills/indie-game-dev/references/sources.md) records the sources behind selected recommendations and explains their scope and verification limits.

## Project status

This repository contains the Skill instructions and supporting references. It does not contain a finished game, a bundled game engine, or a completed function-game prototype. The function-curve example above illustrates one possible way to apply the Skill to a math-related game idea. Any game code, assets, learning outcomes, or playtest results would need to be created and verified in a separate project.
