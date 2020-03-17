![logo](http://i.imgur.com/lVMTcfS.png)


YABEE 14.4
=====
Renewed Egg exporter for the Blender 2.8 and Panda3D

Exporting:
- Meshes
- UV layers
- Materials 
- Vertex colors
- Textures (Diffuse textures and Normal maps)
- Armature (skeleton) animation
- ShapeKeys (morph) animation
- Non-cyclic NURBS Curves

Missing features/TODO
=====
- Properties/tags
- Texture baking via Cycles
- Non-Shader Mode for Materials & Textures

Principled Shader Support
=====
With the addition of the the Principled BSDF shader in Blender and the upcomming support for physically based materials 
in Panda3D it was possible to extend YABEE to improve the workflow for artists when working in a PBR environment. 

<img src="https://i.imgur.com/YaHcdbk.png" />
<p style="font-size: small">Multimeshed object using multple (two) textures in Panda3D</p>

<img src="https://i.imgur.com/iIZNZC8.png" />
<p style="font-size: small">My multimeshed rigged character using multple textures in Panda3D 
(Regular meshes) </p>

<img src="https://i.imgur.com/v37q51J.png" />
<p style="font-size: small">YABEE becomes more Blender-compatible: No special Nodegroup is needed anymore</p>

To use it, you have to create a material for your mesh, set up the Principled BSDF shader 
by connecting at least the Image Texture shader and optionally UV Map.

The PBR node support is still work in progress, if you find important features missing please contact the developers.

**Use this version of YABEE carefully. It doesn't support previous Blender 2.7 versions. It may contain bugs and may not work for objects with complex node system 
applied (something more than UVMap and Texture Image).**

1. **Do backup** of your blend files first or revert the project after exporting.
2. To avoid further issues, don't save your project after export is done. Save it **BEFORE** exporting.

How To Export
=====
Before exporting:

<img src="https://i.imgur.com/gbc0jbB.png" />

1. Select all meshes of the character except armature, or
2. Select all meshes of the character including armature

Experimental Non-Shader Mode for Materials:

This mode doesn't use Nodes.

<img src="https://i.imgur.com/1cOYHvc.png" />
<p style="font-size: small">Disable "Use Nodes" to activate Non-Shader Mode (currently works for PBR render pipelines)</p>
