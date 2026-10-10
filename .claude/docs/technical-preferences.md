# Technical Preferences

<!-- Populated by /setup-engine. Updated as the user makes decisions throughout development. -->
<!-- All agents reference this file for project-specific standards and conventions. -->

## Engine & Language

- **Engine**: Godot 4.7.2
- **Language**: C# (.NET 8+)
- **Rendering**: Compatibility renderer (2D, widest hardware reach incl. mobile)
- **Physics**: Godot Physics 2D (minimal physics use; Jolt applies to 3D only)

## Input & Platform

<!-- Written by /setup-engine. Read by /ux-design, /ux-review, /test-setup, /team-ui, and /dev-story -->
<!-- to scope interaction specs, test helpers, and implementation to the correct input methods. -->

- **Target Platforms**: PC (Steam) at launch; mobile (Android / iOS) port later
- **Input Methods**: Keyboard/Mouse, Touch
- **Primary Input**: Keyboard/Mouse
- **Gamepad Support**: None
- **Touch Support**: Full
- **Platform Notes**: No hover-only interactions (every hover action needs a tap/click equivalent). Large touch targets. UI must scale to small screens for the mobile port. Note: Godot C# export to iOS is experimental and C# cannot export to Web.

## Naming Conventions

- **Classes**: PascalCase (`PlayerController`) — must also be `partial`
- **Variables**: Public properties/fields PascalCase (`MoveSpeed`); private fields `_camelCase` (`_currentHealth`)
- **Methods**: PascalCase (`TakeDamage()`, `GetCurrentHealth()`)
- **Signals/Events**: PascalCase + `EventHandler` suffix (`HealthChangedEventHandler`)
- **Files**: PascalCase matching class (`PlayerController.cs`)
- **Scenes/Prefabs**: PascalCase matching root node (`PlayerController.tscn`)
- **Constants**: PascalCase (`MaxHealth`, `DefaultMoveSpeed`)

## Performance Budgets

- **Target Framerate**: 60 fps
- **Frame Budget**: 16.6 ms
- **Draw Calls**: < 500 per frame (2D)
- **Memory Ceiling**: 1 GB (PC), 512 MB (mobile)

## Testing

- **Framework**: GdUnit4 (gdUnit4Net for C#)
- **Minimum Coverage**: [TO BE CONFIGURED]
- **Required Tests**: Balance formulas, gameplay systems, networking (if applicable)

## Forbidden Patterns

<!-- Add patterns that should never appear in this project's codebase -->
- [None configured yet — add as architectural decisions are made]

## Allowed Libraries / Addons

<!-- Add approved third-party dependencies here -->
- [None configured yet — add as dependencies are approved]

## Architecture Decisions Log

<!-- Quick reference linking to full ADRs in docs/architecture/ -->
- [No ADRs yet — use /architecture-decision to create one]

## Engine Specialists

<!-- Written by /setup-engine when engine is configured. -->
<!-- Read by /code-review, /architecture-decision, /architecture-review, and team skills -->
<!-- to know which specialist to spawn for engine-specific validation. -->

- **Primary**: godot-specialist
- **Language/Code Specialist**: godot-csharp-specialist (all .cs files)
- **Shader Specialist**: godot-shader-specialist (.gdshader files, VisualShader resources)
- **UI Specialist**: godot-specialist (no dedicated UI specialist — primary covers all UI)
- **Additional Specialists**: godot-gdextension-specialist (GDExtension / native C++ bindings only)
- **Routing Notes**: Invoke primary for architecture decisions, ADR validation, and cross-cutting code review. Invoke C# specialist for code quality, [Signal] delegate patterns, [Export] attributes, .csproj management, and C#-specific Godot idioms. Invoke shader specialist for material design and shader code. Invoke GDExtension specialist only when native C++ plugins are involved.

### File Extension Routing

<!-- Skills use this table to select the right specialist per file type. -->
<!-- If a row says [TO BE CONFIGURED], fall back to Primary for that file type. -->

| File Extension / Type | Specialist to Spawn |
|-----------------------|---------------------|
| Game code (.cs files) | godot-csharp-specialist |
| Shader / material files (.gdshader, VisualShader) | godot-shader-specialist |
| UI / screen files (Control nodes, CanvasLayer) | godot-specialist |
| Scene / prefab / level files (.tscn, .tres) | godot-specialist |
| Project config (.csproj, NuGet) | godot-csharp-specialist |
| Native extension / plugin files (.gdextension, C++) | godot-gdextension-specialist |
| General architecture review | godot-specialist |
