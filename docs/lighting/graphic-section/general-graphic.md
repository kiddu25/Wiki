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

*Source's native cubemap implementation does not allow them to follow the player's perspective. While this is passable in most cases, tying the reflections to the player's view can increase realism, especially when using high-resolution reflections. A method to achieve this is called parallax correction.

Parallax-corrected cubemaps use a bounding box brush to bake their reflection based on a specified area around them, and a custom shader to make use of it.


without:

with:


### Physically Based Rendering (PBR)

* 

### Parallax Occlusion Mapping(POC)

*Parallax mapping (also known as offset mapping or virtual displacement mapping) is a shading technique that displaces the individual pixel height of a surface so that when you look at it at an angle, the high points will obscure the low points behind them, making it look three-dimensional. The height data for each pixel comes from a $parallaxmap texture, which needs to be created for each parallax mapped material.



### "My dynamic shadows update in low fps"

* There is a cap on how many faces can get their shadows updated, and this cap is called the **shadow frame budget**. This is an optimization technique that prevents the game from lagging on low-end devices. You can increase the budget by using the `r_clustered_shadowframebudget` console command. Note that this will significantly lower your fps when used carelessly.

### "Shadows glitch or flicker when a light is moving"

* Clustered shadows update less frequently than the game itself, so if a moving clustered light entity cannot keep up updating the shadowmap, the shadows from that entity will flicker. This often happens in heavy maps with a lot of clustered lights, and rarely if the light peaks from a corner, especially when lighting up a huge area. There is no workaround other than not moving clustered lights too fast and using dynamic shadows only where necessary.

### "Everything is completely broken/corrupted and I can't fix it"

* Certain GPU models may have trouble running the clustered renderer. **If you experience this, let us know what GPU brand/model, operating system and other hardware specs you're using.** Clustered lights may act weird when running the game on Linux under DXVK on AMD platforms. However, the circumstances in which they break should not be possible in production.

## If you have any issues that are not addressed in this article, make sure to report it to us on the [Strata issue tracker.](https://github.com/StrataSource/Engine/issues)
