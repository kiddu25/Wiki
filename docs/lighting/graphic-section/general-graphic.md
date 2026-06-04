---
title: "General Graphic"
weight: 20
---

# General Graphic

[!NOTE]

*Strata Source is only  64-bit 

*Strata Source run on Directx 11, it's mean that graphical feature that you will see are possible (e.g cluster lighting)

### Cascade Shadows Mapping(CSM)
* It casts an extremely accurate shadow map via the tools/toolsskybox texture, augmenting the lighting cast by light_environment with real-time shadows. This form of shadow mapping is known as Cascaded Shadow Maps, or CSM for short, which works by rendering very detailed shadow maps which becomes a lower and lower resolution depending on the distance the viewer is from the surface, similar to mipmaps. Some games automatically add this entity to the map, but it can be placed manually as well.
par

without :

with : 

### Parallax Corrected Cubemaps(PCC)

*The Original implementation cubemaps does not allow them to follow the player's perspective, making Reflection not accurate, Follow the reflection to the player's view make improve the realism, especially when using high-resolution reflections. A method to achieve this is called parallax correction.

Parallax-corrected cubemaps use a bounding box brush to bake their reflection based on a specified area around them.


without:

with:


### Physically Based Rendering (PBR)

* 

### Parallax Occlusion Mapping(POC)

*Parallax mapping (also known as offset mapping or virtual displacement mapping) is a shading technique that displaces the individual pixel height of a surface so that when you look at it at an angle, the high points will obscure the low points behind them, making it look three-dimensional. The height data for each pixel comes from a $parallaxmap texture, which needs to be created for each parallax mapped material.

###SSAO(xegtao)

###Volumetric

###cluster forwards and volumetric


###Light cooking


