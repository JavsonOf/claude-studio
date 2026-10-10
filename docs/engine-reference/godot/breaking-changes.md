# Godot — Breaking Changes

Last verified: 2026-10-10

Changes between Godot versions, focused on post-LLM-cutoff changes (4.4+).

## 4.6 → 4.7 (Jun 2026 — POST-CUTOFF, HIGH RISK)

Source: https://docs.godotengine.org/en/stable/tutorials/migrating/upgrading_to_godot_4.7.html
Official verdict: "relatively safe to migrate" for most 4.6 projects.
C# columns: **Bin** = binary compatible, **Src** = source compatible (❌ = code must change).

### Breaking API changes

| Subsystem | Change | GDScript | C# Bin | C# Src |
|-----------|--------|----------|--------|--------|
| Core | `Object.is_class` param `class` type `String` → `StringName` | ✔️ | ✔️ | ✔️ |
| Core | `ZIPPacker.start_file` adds optional `permissions`, `modified_time` | ✔️ | ✔️ | ✔️ |
| Core | `OptimizedTranslation.generate` returns `bool` (was `void`) | ✔️ | ❌ | ✔️ |
| 2D/3D | `CPUParticles*/GPUParticles*.request_particles_process` adds optional `process_time_residual` | ✔️ | ✔️ | ✔️ |
| GUI | `Control.accessibility_live` type `DisplayServer.AccessibilityLiveMode` → `AccessibilityServer.AccessibilityLiveMode` | ✔️ | ❌ | ❌ |
| GUI | `RichTextLabel` enum `ImageUpdateMask.UPDATE_WIDTH_IN_PERCENT` → `UPDATE_WIDTH_UNIT` | ❌ | ✔️ | ❌ |
| GUI | `RichTextLabel.add_image` / `update_image`: `width`/`height` `int` → `float` | ✔️ | ✔️ | ✔️ |
| GUI | `RichTextLabel.add_image` / `update_image`: `width_in_percent`/`height_in_percent` (`bool`) → `width_unit`/`height_unit` (`RichTextLabel.ImageUnit`) | ✔️ | ✔️ | ❌ |
| Text | `Font.find_variation` adds optional `palette_index`, `custom_colors` | ✔️ | ✔️ | ✔️ |
| Text | `TreeItem.select` adds optional `set_as_cursor` | ✔️ | ✔️ | ✔️ |
| Rendering | `ImageTexture.get_format` / `PortableCompressedTexture2D.get_format` moved to base `Texture2D` | ✔️ | ✔️ | ✔️ |
| Rendering | `RenderingServer.particles_request_process_time`: `time` → `process_time`, adds `process_time_residual` | ✔️ | ✔️ | ❌ |
| Rendering | `RenderingServer.viewport_set_size` adds optional `view_count` | ✔️ | ✔️ | ✔️ |
| Rendering | `Image.save_exr` / `save_exr_to_buffer` add optional `color_image`, `max_linear_value` | ✔️ | ✔️ | ✔️ |
| Animation | `Animation.length` type metadata `float` → `double` | ✔️ | ❌ | ❌ |
| Animation | `AnimationNodeBlendSpace1D/2D.add_blend_point` adds optional `name` | ✔️ | ✔️ | ✔️ |
| Physics | `PhysicsServer2D.body_set_shape_as_one_way_collision` adds optional `direction` | ✔️ | ✔️ | ✔️ |
| Physics | `PhysicsServer2DExtension._body_set_shape_as_one_way_collision` adds `direction` | ❌ | ❌ | ❌ |
| Audio | `AudioEffectSpectrumAnalyzer.tap_back_pos` removed | ❌ | ❌ | ❌ |
| XR | `OpenXRExtensionWrapper._on_register_metadata` adds `interaction_profile_metadata` | ❌ | ❌ | ❌ |
| Editor | `EditorSceneFormatImporter.IMPORT_*` constants moved into enum `ImportFlags` | ✔️ | ✔️ | ❌ |
| Editor | `EditorVCSInterface._commit` adds `amend` | ❌ | ❌ | ❌ |

### Behavior changes

| Subsystem | Change |
|-----------|--------|
| Rendering | `CanvasItem` no longer adds an antialiasing feather when drawing lines — lines look thinner; increase width if you relied on it |
| Rendering | `LinearToSRGB` visual shader no longer clamps to `[0, 1]` on Mobile / Forward+ |
| Input | Mouse/keyboard device IDs changed from `0` to `InputEvent.DEVICE_ID_MOUSE` / `InputEvent.DEVICE_ID_KEYBOARD` — check event type or compare to these constants, never `device == 0` |
| Audio | `AudioStreamPlayer.area_mask` default `1` → `0`; reset to layer 1 if you use `Area2D/3D` audio bus override |
| Physics (Jolt 3D) | `WorldBoundaryShape3D.plane.d` sign flipped; `SoftBody3D` mass/stiffness changes; `Area3D` reports `SoftBody3D` overlaps |
| GDScript | Packed array element set no longer calls whole-property setter; overrides inherit typed return (need explicit `return`) |

### Changed defaults

| Property | Old | New |
|----------|-----|-----|
| New projects: `display/window/stretch/mode` / `aspect` | `disabled` / `keep` | `canvas_items` / `expand` |
| `ResourceImporterDynamicFont.hinting` | 1 | 3 |
| `RichTextLabel.add_image`/`update_image` `width_in_percent`/`height_in_percent` | false | 0 |
| `ProjectSettings rendering/reflections/sky_reflections/roughness_layers` | 7 | 8 |
| `LookAtModifier3D.relative` | true | false |

### Notable new features (non-breaking)

| Subsystem | Feature |
|-----------|---------|
| GUI | `Control.offset_transform_*` — move/rotate/scale a Control without its parent Container resetting it (animated menus, button feedback) |
| 2D | `DrawableTexture2D` for simple texture drawing; Scene Paint tool for painting scenes into levels |
| Rendering | HDR output for 2D and 3D; `AreaLight3D` |
| Editor | New Asset Store replaces the Asset Library |
| Input | Built-in `VirtualJoystick` node |
| Accessibility | Landmark navigation for screen readers |
| Platform | Improved Android-on-device development and publishing |

## 4.5 → 4.6 (Jan 2026 — POST-CUTOFF, HIGH RISK)

| Subsystem | Change | Details |
|-----------|--------|---------|
| Physics | Jolt is now the DEFAULT 3D physics engine | New projects use Jolt automatically. Existing projects keep their setting. Some HingeJoint3D properties (like `damp`) only work with GodotPhysics. |
| Rendering | Glow processes BEFORE tonemapping | Was after tonemapping. Scenes with glow will look different. Adjust intensity/blend in WorldEnvironment. |
| Rendering | D3D12 default on Windows | Was Vulkan. For better driver compatibility. |
| Rendering | AgX tonemapper new controls | White point and contrast parameters added. |
| Core | Quaternion initializes to identity | Was zero. Unlikely to affect most code but technically breaking. |
| UI | Dual-focus system | Mouse/touch focus now separate from keyboard/gamepad focus. Visual feedback differs by input method. |
| Animation | IK system fully restored | CCDIK, FABRIK, Jacobian IK, Spline IK, TwoBoneIK via SkeletonModifier3D nodes. |
| Editor | New "Modern" theme default | Grayscale replaces blue-tint. Restore: Editor Settings → Interface → Theme → Style: Classic |
| Editor | "Select Mode" keybind changed | New "Select Mode" (v key) prevents accidental transforms. Old mode renamed "Transform Mode" (q key). |
| 2D | TileMapLayer scene tile rotation | Scene tiles can now be rotated like atlas tiles. |
| Localization | CSV plural form support | No longer requires Gettext for plurals. Context columns added. |
| C# | Automatic string extraction | Translation strings auto-extracted from C# code. |
| Plugins | New EditorDock class | Specialized container for plugin docks with layout control. |

## 4.4 → 4.5 (Late 2025 — POST-CUTOFF, HIGH RISK)

| Subsystem | Change | Details |
|-----------|--------|---------|
| GDScript | Variadic arguments added | Functions can accept `...` arbitrary params — new language feature |
| GDScript | `@abstract` decorator | Abstract classes and methods now enforceable |
| GDScript | Script backtracing | Detailed call stacks available even in Release builds |
| Rendering | Stencil buffer support | New capability for advanced visual effects |
| Rendering | SMAA 1x antialiasing | New post-processing AA option |
| Rendering | Shader Baker | Pre-compiles shaders — reportedly 20x faster startup on some demos |
| Rendering | Bent normal maps, specular occlusion | New material features |
| Accessibility | Screen reader support | Control nodes work with accessibility tools via AccessKit |
| Editor | Live translation preview | Test GUI layouts in different languages in-editor |
| Physics | 3D interpolation rearchitected | Moved from RenderingServer to SceneTree. API unchanged but internals differ. |
| Animation | BoneConstraint3D | New: AimModifier3D, CopyTransformModifier3D, ConvertTransformModifier3D |
| Resources | `duplicate_deep()` added | New explicit method for deep duplication of nested resources |
| Navigation | Dedicated 2D navigation server | No longer a proxy to 3D navigation; smaller export for 2D games |
| UI | FoldableContainer node | New accordion-style container for collapsible UI sections |
| UI | Recursive Control behavior | Disable mouse/focus interactions across entire node hierarchies |
| Platform | visionOS export support | New platform target |
| Platform | SDL3 gamepad driver | Delegated gamepad handling to SDL library |
| Platform | Android 16KB page support | Required for Google Play targeting Android 15+ |

## 4.3 → 4.4 (Mid 2025 — NEAR CUTOFF, VERIFY)

| Subsystem | Change | Details |
|-----------|--------|---------|
| Core | `FileAccess.store_*` return `bool` | Was `void`. Methods: `store_8`, `store_16`, `store_32`, `store_64`, `store_buffer`, `store_csv_line`, `store_double`, `store_float`, `store_half`, `store_line`, `store_pascal_string`, `store_real`, `store_string`, `store_var` |
| Core | `OS.execute_with_pipe` | Added optional `blocking` parameter |
| Core | `RegEx.compile/create_from_string` | Added optional `show_error` parameter |
| Rendering | `RenderingDevice.draw_list_begin` | Many parameters removed; `breadcrumb` parameter added |
| Rendering | Shader texture types | Parameter/return types changed from `Texture2D` to `Texture` |
| Particles | `.restart()` method | Added optional `keep_seed` parameter (CPU/GPU 2D/3D) |
| GUI | `RichTextLabel.push_meta` | Added optional `tooltip` parameter |
| GUI | `GraphEdit.connect_node` | Added optional `keep_alive` parameter |

## 4.2 → 4.3 (In Training Data — LOW RISK)

| Subsystem | Change | Details |
|-----------|--------|---------|
| Animation | `Skeleton3D.add_bone` returns `int32` | Was `void` |
| Animation | `bone_pose_updated` signal | Replaced by `skeleton_updated` |
| TileMap | `TileMapLayer` replaces `TileMap` | One node per layer instead of multi-layer single node |
| Navigation | `NavigationRegion2D` | Removed `avoidance_layers`, `constrain_avoidance` properties |
| Editor | `EditorSceneFormatImporterFBX` | Renamed to `EditorSceneFormatImporterFBX2GLTF` |
| Animation | AnimationMixer base class | AnimationPlayer and AnimationTree now extend AnimationMixer |
