# Godot Engine — Version Reference

| Field | Value |
|-------|-------|
| **Engine Version** | Godot 4.7.2 |
| **Release Date** | 4.7: June 18, 2026 · 4.7.2: August 18, 2026 |
| **Project Pinned** | 2026-10-10 |
| **Last Docs Verified** | 2026-10-10 |
| **Risk Level** | HIGH — version is beyond LLM training data |
| **LLM Knowledge Cutoff** | May 2025 |

## Knowledge Gap Warning

The LLM's training data likely covers Godot up to ~4.3. Versions 4.4, 4.5,
4.6 and 4.7 introduced significant changes that the model does NOT know about.
Always cross-reference this directory before suggesting Godot API calls.

## Post-Cutoff Version Timeline

| Version | Release | Risk Level | Key Theme |
|---------|---------|------------|-----------|
| 4.4 | ~Mid 2025 | MEDIUM | Jolt physics option, FileAccess return types, shader texture type changes |
| 4.5 | ~Late 2025 | HIGH | Accessibility (AccessKit), variadic args, @abstract, shader baker, SMAA |
| 4.6 | Jan 2026 | HIGH | Jolt default, glow rework, D3D12 default on Windows, IK restored |
| 4.7 | Jun 2026 | HIGH | HDR output, Control offset transforms, RichTextLabel image API, AccessibilityServer, new Asset Store, stretch mode defaults |

## Verified Sources

- Official docs: https://docs.godotengine.org/en/stable/
- 4.6→4.7 migration: https://docs.godotengine.org/en/stable/tutorials/migrating/upgrading_to_godot_4.7.html
- 4.5→4.6 migration: https://docs.godotengine.org/en/stable/tutorials/migrating/upgrading_to_godot_4.6.html
- 4.4→4.5 migration: https://docs.godotengine.org/en/stable/tutorials/migrating/upgrading_to_godot_4.5.html
- Changelog: https://github.com/godotengine/godot/blob/master/CHANGELOG.md
- Release notes: https://godotengine.org/releases/4.7/ (and https://godotengine.org/releases/4.6/)
- Builds / point releases: https://github.com/godotengine/godot-builds/releases

## Project Notes (C#)

- Project language is C#. C# export to Android and iOS is still marked
  experimental (Android needs .NET 7+, iOS needs .NET 8+ and a macOS machine).
  C# projects cannot export to Web.
  Source: https://github.com/godotengine/godot-docs/blob/master/tutorials/scripting/c_sharp/index.rst
