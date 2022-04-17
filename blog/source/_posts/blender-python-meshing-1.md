---
title: Blender-Python API Meshing (1)
date: 2022-04-16 19:29:34
tags: [Blender, Python, Modelling]
categories: Blender

---
[toc]
# Blender-Python API Meshing
- Blender is a free and open-source 3D computer graphics software toolset used for creating animated films, visual effects, art, 3D-printed models, motion graphics, interactive 3D applications, virtual reality, and, formerly, video games.
  
It is a tutorial to teach you how to create mesh by Blender-Python.

First of all, to be able to use the Blender-Python API, you need to import the **bpy** library.

```python
import bpy
```

When you open your new blender python, you can find a cube in the origin. And there is only one area for operating. What we are going to do is to create two new areas. 
<figure>
<img src = '/blog/source/img/1.jpg', width = 300>
<img src = '/blog/source/img/2.jpg', width = 300>
<img src = '/blog/source/img/3.jpg', width = 300>
</figure>
And set the different regions like the figure shown below. It's my personal preferrence, you can set the region as your like. 
<img src = '/blog/source/img/5.jpg'>

Let's firstly use the python console.
```bash
>>> bpy.data.objects
<bpy_collection[3], BlendDataObjects>

>>> bpy.data.objects.keys()
['Camera', 'Cube', 'Light']
