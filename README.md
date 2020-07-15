# UnityURP-MobileScreenSpacePlanarReflection
 ScreenSpacePlanarReflection(SSPR) as a reusable RendererFeature in URP.

 Can run within a few ms on most android mobile devices
 
 SSPR ON
 ![screenshot](https://i.imgur.com/cNaVHLK.png)
 SSPR OFF
 ![screenshot](https://i.imgur.com/0WCIcTM.png)
 SSPR ON
 ![screenshot](https://i.imgur.com/XvudHkR.png)
 SSPR OFF
 ![screenshot](https://i.imgur.com/AZ08hZ8.png)
 Where are the important files?
-------------------
 There are only 3 important code files, all inside a folder "Assets \ _MobileSSPR \ ReusableCore".
 Other files are for demo only, not important.
 
 Can it run on mobile?
-------------------
 Tested on ~10 android devices, should we alright if your android device support OpenGLES3.2 / Vulkan.
 
 How to try this in my own URP project?
 -------------------
 - find 3 important code files inside "Assets \ _MobileSSPR \ ReusableCore" folder, copy them to your project
 - turn on "Depth Texture" in URP's setting
 - turn on "Opaque Texture" in URP's setting
 - Add MobileSSPRRendererFeature(RendererFeature) to your forward renderer asset
 - assign MobileSSPRComputeShader to this new RendererFeature's "compute shader" slot
 - create a new plane game object in your scene (set world space pos y = 0)
 - create a material using MobileSSPRExampleShader
 - put this material to the plane
 - DONE!

 Notes
 -------------------
 It is just a quick proof of concept project to test if screen space reflection & compute shader can run on mobile correctly and fast enough.
 
 Editor
 -------------------
2019.4.3f1 LTS

Implementation reference
-------------------
http://remi-genin.fr/blog/screen-space-plane-indexed-reflection-in-ghost-recon-wildlands/
 
 
