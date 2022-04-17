---
title: Blender-Python API Meshing (1)
date: 2022-04-16 19:29:34
tags: [Blender, Python, Modelling]
categories: Blender

---
[toc]
# Blender-Python API Meshing
## A Brief Introduction
- Blender is a free and open-source 3D computer graphics software toolset used for creating animated films, visual effects, art, 3D-printed models, motion graphics, interactive 3D applications, virtual reality, and, formerly, video games.
  
It is a tutorial to teach you how to create mesh by Blender-Python.

First of all, to be able to use the Blender-Python API, you need to import the **bpy** library.

```python
import bpy
```

When you open your new blender python, you can find a cube in the origin. And there is only one area for operating. What we are going to do is to create two new areas. 
<figure>
<img src = 'https://raw.githubusercontent.com/HuJacobJiabao/HuJacobJiabao.github.io/main/blog/source/img/1.jpg'>
<img src = 'https://raw.githubusercontent.com/HuJacobJiabao/HuJacobJiabao.github.io/main/blog/source/img/2.jpg'>
<img src = 'https://raw.githubusercontent.com/HuJacobJiabao/HuJacobJiabao.github.io/main/blog/source/img/3.jpg'>
</figure>
And set the different regions like the figure shown below. It's my personal preferrence, you can set the region as your like. 
<img src = 'https://raw.githubusercontent.com/HuJacobJiabao/HuJacobJiabao.github.io/main/blog/source/img/5.jpg'>

### Python Console
Let's firstly use the python console.
```bash
>>> bpy.data.objects
<bpy_collection[3], BlendDataObjects>

>>> bpy.data.objects.keys()
['Camera', 'Cube', 'Light']
```
And we can assign the object `'Cube'` to a variable `cube`. And move the cube to another position.
```bash
>>> cube = bpy.data.objects['Cube']
>>> cube.location
Vector((0.0, 0.0, 0.0))

>>> cube.location = (1, 1, 1)
```
Then the centroid of the cube will move to `(1, 1, 1)`.
### Text Editor
The operations above can be done by using the script in the text editor.
```python
import bpy

cube = bpy.data.objects['Cube']
cube.location = (1, 1, 1)
```