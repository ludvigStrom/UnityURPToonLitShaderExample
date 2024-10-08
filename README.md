# About this repository

This is a fork of the NiloToonURP released under MIT 

MIT License

Copyright (c) 2020 ColinLeung-NiloCat

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.





This repository does NOT contain the full version of NiloToonURP.  
Instead, it includes a simple, short and easy-to-read URP toon shader example for Unity2022.3LTS, which is intended for shader coding tutorial purposes. The shader example is licensed under the MIT license, giving you the freedom to use the code as you wish. If you'd like to retain the current tutorial shader, we recommend forking it or downloading a copy now, as it may be removed in the future.  
  
*this README also shows photos and information about the NiloToonURP(full version)

# NiloToonURP(full version)'s rendering

We are now developing an 'easy-to-use, high-performance, and cross-platform (including mobile, VR, and WebGL)' closed-source toon shader package—NiloToonURP—to assist Unity URP users in achieving high-quality anime/toon-like rendering.

NiloToonURP is supporting:
- Unity 2021.3LTS(URP 12.x)
- Unity 2022.3LTS(URP 14.x)
- Unity 2023.2 (URP 16.x)
- Unity6 (URP 17.x)

# Download NiloToonURP PC .exe demo (2021.3.17LTS build):
- https://drive.google.com/file/d/1MubGDhlDRKKxR9xyl7fcLyECyBJdsqrI/view?usp=sharing  

# Download NiloToonURP Android .apk demo (2021.3.17LTS build):
- https://drive.google.com/file/d/1CBSYiniHTAaNtlkd5X7TUxjAsQ7eBNxK/view?usp=sharing

# NiloToonURP's demo runtime video: 
- https://www.youtube.com/c/colinleungNiloCat/videos
- https://space.bilibili.com/325873

# NiloToonURP's UI preview: 
- https://drive.google.com/drive/folders/1SlOhvqCZrDBRkSgzwW0ZIzAkDqonpa26?usp=sharing

# How to get NiloToonURP full source code?
If you or your company/organization/team needs: 
- latest full source code (with all detail comments and notes, NOT Obfuscated code, NOT .dll)
- latest user document
- perpetual royalty-free commercial license
- every future update
- NiloToon's tech support
- (optional) we set up your character models's rendering in the best way possible for you, using NiloToonURP
- (optional) your project-specific customization and support 

of NiloToonURP for your URP project, please send the following info to nilotoon@gmail.com
- name (your personal name or your company/organization/team's name)
- a google account email for gaining permission to download all NiloToonURP files in google drive
- any public website that shows your/your company/organization/team's work or public media (e.g. personal website/company website/youtube/bilibili/twitter...) 

# NiloToonURP user's creations (public media, not NDA content)
*we only provided NiloToonURP's download permission + tech support, we didn't work on these creations directly

What is included in this simplified tutorial example toon-lit shader repository?
-------------------
This repository only contains a very simple toon-lit URP tutorial shader example, to help people write their first custom toon-lit shader in URP.

This example shader's default result(without editing material params) = the following picture
![screenshot](https://i.imgur.com/7vo6Duo.jpg)

Because this example toon lit shader aims to help people learn shader writing in URP, it is an extremely simplified version. This repository only contains ~3% of the NiloToonURP(full version)'s code, which only contains the most basic & easily understandable sections, to make sure everyone can understand the shader code easily.

It is actually a "How to write your first custom toon-lit shader in URP?" example, instead of a good-looking toon-lit shader (lots of toon-lit tricks are not included in this example shader, for tutorial reasons).

Why create this "simplified version" toon lit shader?
-------------------
Lots of my shader friends are looking for a toon-lit example shader in URP (not Shader Graph), I want them to switch to URP(instead of still staying in built-in RP), so I decided to provide a simple enough URP toon-lit shader example in URP. 

How to try this simplified toon-lit example shader in my URP project?
-------------------
1. Clone all .shader & .hlsl files into your URP project.
2. Put these files inside the same folder.
3. Change your character's material's shader to "SimpleURPToonLitExample(With Outline)"
4. make sure at least _BaseMap(albedo) is assigned
5. setup DONE, you can now test your character with light probe/directional light/point light/spot light
6. edit the material properties to see how the render result changes
7. Most important: open these shader files, and spend some time reading them, you will understand how to write custom lit shaders in URP very quickly
8. Most important: open "SimpleURPToonLitOutlineExample_LightingEquation.hlsl", edit it, and experiment with your own toon lighting equation ideas, which is the key part of toon lit shader!

I see the shader is working now, but the outline is broken?
-------------------
For this tutorial shader, you can let Unity calculate smoothed normal for you, which can produce a better outline, 
but doing this will make the lighting slightly incorrect.

1. click your character's .fbx
2. In the model tab
3. edit "Normals" to Calculate
4. edit "Smoothing Angle" to 180  
  
![screenshot](https://i.imgur.com/rqefuLr.jpg)  
before calculating smooth normal (print screen of the tutorial shader, not NiloToonURP)  
![screenshot](https://i.imgur.com/wbjjNtF.jpg)  
after calculating smooth normal  (print screen of the tutorial shader, not NiloToonURP)
![screenshot](https://i.imgur.com/fTscZV0.jpg)

*NiloToonURP(full version) contains many editor/runtime C# scripts, some of them are for producing correct lighting and perfect outline together automatically.

What is NOT included in this simplified tutorial shader?
-------------------
For simplicity reasons, most of the features from the NiloToonURP(full version) are removed, or else for beginners, this simple tutorial example shader will be way too complex for reading & learning. Some of the removed features are:
- face anime lighting (auto-fix face ugly lighting due to vertex normal without modifying .fbx, very important)
- smooth outline normal auto baking (auto-fix ugly outlines without modifying .fbx and lighting normal, very important)
- auto 2D hair shadow on the face (very important, it is very difficult to produce good-looking shadow results on the face using URP's shadow map)
- constant width rim light (similar to the method of Blue Protocol / Genshin Impact)
- tricks to render eye/eyebrow over hair (ZOffset, stencil, and renderer redraw helpers)
- PBR specular lighting (GGX)
- all kinds of MatCap features(additive/multiply/shadow/replace...)
- "HSV,tint,texture tint,texture override" shadow & outline color control
- almost all the extra texture input options like roughness, specular, normal map, detail map, parallax, occlusion, emission...
- LOTS of sliders to control lighting style, shadow color, final color, outline, rim light...
- per character "dither fade inout / rim light / color control / extra outline / dissolve /  ..." control script
- volume override control of global "rim light / shadow / color control..."
- special bloom post-process volume that can control the param of character/non-character area separately. Usually to prevent character over-bloom, or make the character emitting bloom on allowed areas only
- anime postprocessing volume
- shadow control volume
- perspective removal per character, to avoid character's 3D distorted by high FOV camera
- shader stripping editor script, to keep runtime shader memory usage and build time lower
- (lots of other features)
* just too much for me to write all the removed features here, the NiloToonURP(full version) and this simple tutorial shader example are two totally different products already

How to get a test character model?
-------------------
The easiest way to get a character model is by downloading Unity-Chan in the Unity AssetStore.

Also, here are some websites where you can download models(If the creator allows it)
- https://3d.nicovideo.jp/
- https://hub.vroid.com/

if you downloaded a .pmx file, use MMD4Mecanim to convert it to .fbx & prefab directly inside unity
http://stereoarts.jp/

if you downloaded a .vrm file, use UniVRM to convert it to prefab directly inside Unity
https://github.com/vrm-c/UniVRM

Editor version requirement
-----------------------
- Unity 2022.3

---------------------------
Apply our shader to another model (2020-2 early version screenshots)
https://youtu.be/uVI_QOioER4
