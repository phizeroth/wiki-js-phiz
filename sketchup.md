---
title: sketchup
description: 
published: true
date: 2020-08-02T16:02:43.444Z
tags: 
editor: undefined
---


# SketchUp notes

Test embedded model from 3D Warehouse:
<iframe src="https://3dwarehouse.sketchup.com/embed/7e968057-b5a0-4f52-8953-2820d2d5cb94" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" width="580" height="326" allowfullscreen></iframe>

## extensions
Some of my favorite plugins:

- [Auto Invisible Layer](https://extensions.sketchup.com/en/content/auto-invisible-layer) \-- When enabled, changes SketchUp's default behavior of new layers being enabled in all scenes.  Disabled by default at the start of each session.
- [Turn Off Layer In All Scenes (TOLIAS)](https://sketchucation.com/forums/viewtopic.php?f=80&t=66243) --  Turns off the _active_ layer in all scenes.  I also made a slighty edited version which turns a layer ON in all scenes.
- [Solid Inspector²](https://extensions.sketchup.com/en/content/solid-inspector%C2%B2) -- _"Select a group or component and activate the tool for an analysis of what would prevent it from being a solid manifold."_ An example usage: Solid Tools such as Trim require objects to be true solids.
- [Material Tools](https://extensions.sketchup.com/en/content/material-tools) -- requires [TT\_Lib²](https://extensions.sketchup.com/content/tt_lib%C2%B2)
- [Material Replacer](https://extensions.sketchup.com/en/content/material-replacer) -- _"Replace one material for another by picking material in the model"_ -- requires [TT\_Lib²](https://extensions.sketchup.com/content/tt_lib%C2%B2)
- [CleanUp³](https://extensions.sketchup.com/en/content/cleanup%C2%B3) -- fix / purge / merge / repair -- requires [TT\_Lib²](https://extensions.sketchup.com/content/tt_lib%C2%B2)
- [Eneroth Solid Tools](https://extensions.sketchup.com/pl/content/eneroth-solid-tools) -- _"Solid tools designed to feel more native to SketchUp than the native solid tools."_
- [Axes Tools](https://extensions.sketchup.com/en/content/axes-tools) -- _"Small utilty that reset the axis of components to their bounding box' centre or corners."_
- [Eneroth Component Replacer ](https://extensions.sketchup.com/en/content/eneroth-component-replacer) -- _"Swiftly pick up any component or group and replace others with it."_
- [FredoScale](https://extensions.sketchup.com/en/content/fredoscale) _-- "...Orientate the selection box around a set of objects and interactively apply a number of geometric transformations, such as Scaling, Tapering, Stretching, Plane Shear, Twisting, Bending and Rotation..."_ -- Requires [LibFredo](https://extensions.sketchup.com/en/content/libfredo6)
- [FredoGhost](https://sketchucation.com/plugin/2191-fredoghost) -- Automates proxy modelling, temporarily swapping complex models with simplified "ghost" versions which are generated by the plugin. This improves performance, and also allows display of multiple styles at once. -- Requires [LibFredo](https://extensions.sketchup.com/en/content/libfredo6)

Here's some interesting extensions I haven't tried yet:  

- Selection Toys( [sketchucation](https://sketchucation.com/plugin/738-tt_selection_toys) )
- Architect Tools ([warehouse](https://extensions.sketchup.com/extension/0e2b5a47-add9-47c7-894b-9be1e046cfba/architect-tools))
- TrueBend ([warehouse](https://extensions.sketchup.com/extension/c9135b56-4492-449e-ac63-8c26b734ba39/truebend) / [sketchucation](https://sketchucation.com/pluginstore?pln=tt_truebend))
- ClothWorks ([sketchucation](https://sketchucation.com/plugin/2053-clothworks))
- Eneroth Fractal Terrain Eroder ([warehouse](https://extensions.sketchup.com/extension/a609a3c3-4066-42b9-98aa-9d4ecdb19287/eneroth-fractal-terrain-eroder) / [sketchucation](https://sketchucation.com/plugin/720-ene_fractalterrain_v1-0-0_2))
- Profile Builder ([website](https://profilebuilder4sketchup.com/))
- Weld
- Vertex Tools
- Quad Face Tool
- Split Donut / Split Sausage
- SubD
- Joint Push Pull
- FredoCorner / Round corners
- Push Line
## keyboard shortcuts
My essential tools / commands, and the keyboard shortcut I have assigned to each.  I use a [WASD] hand position (gaming-style), and have chosen shortcuts based on ergonomics / frequency of use.

I've swapped a couple of keys around on the keyboard, using [Sharpkeys]:
  - `Control` <--> `Caps`
  - `Esc` <--> `~`
  
<details>
  <summary><b>View table of shortcuts:</b></summary>
  
command     | key binding
------------|------------
space       | Selection tool
V           | Move
C           | Line
D           | Push/Pull
Q           | Rotate
S           | Scale
R           | Rectangle
shift-C     | Circle
shift-R     | Offset
B           | Paint Bucket (hold ALT to sample material)
shift-E     | Eraser
Z           | Undo
shift-Z     | Redo
shift-V     | Paste in Place
W           | Make Group
shift-W     | Make Component
ctrl-R      | Make Unique
A           | Hide Rest of Model
shift-Q     | Update Scene
shift-T     | Trim
alt-Z       | Zoom Extents
E           | UI - Toggle Entity Info (I use a loose tray window for Entity Info)
alt-A       | UI - Show Outliner Tab
alt-S       | UI - Show Layers Tab
alt-D       | UI - Show Scenes Tab
  
</details>

## Proxy modeling
- [Video: Sketchup Skill-Builder - proxy with native SU tools](https://youtu.be/2VZj-odqx68)
- [Article: Always Use Proxy Components in Sketchup for Faster Rendering](http://sketchup-ur-space.com/2017/dec/always-use-proxy-components-in-sketchup-for-faster-rendering.html)
- [Fredo Ghost extension](https://sketchucation.com/plugin/2191-fredoghost)

[WASD]: https://raw.githubusercontent.com/bubbavox/notes_public/master/images/WASD.jpg
[Sharpkeys]: https://www.randyrants.com/category/sharpkeys/
