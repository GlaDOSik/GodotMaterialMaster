# GodotMaterialMaster

**Allows user to globaly override custom materials in all imported scenes.**

This plugin simplifies the workflow when all models are imported from GLB file but materials are made in Godot.

When GLB file with models is imported as scene, we have only 3 options how to handle materials:
- use material from GLB file (material made outside of Godot)
- override material per whole MeshInstance (material made inside Godot)
- extract materials from import dialog and adjust them in editor (material made inside Godot)

Overriding material per whole mesh instance may be good enough in many cases, but if your model contains more than 1 material, this option won't work for you.
The last option allows user to override material per surface, but the process is clunky. Not only you have to manually extract materials for each new GLB file, the extract process will create base material by default. If you want to create
shader material, you have to replace the extracted material with the new one. And if you want to reuse your material in different file, you have to manually fiddle with import files. Good luck if you want rename file with material or material
name in Blender later, when many references are already made.

Material Master adjusts the import files under the hood for you in order to automatically update all metarial overrides in your project.
