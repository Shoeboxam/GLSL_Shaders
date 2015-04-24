GLSL Shaders for Invictus

A collection of fragment shaders that operate on every pixel of every frame. These use Minecraft's json files to set up input samplers and access specific coordinates. Each fragment, or pixel, is calculated concurrently in separate threads on the GPU.  

Guiding principles: no branching constructs, use dot products, use built-ins, use MAD, limit samples  

Invictus_phosphor:  Smooth multiple frames together  
Invictus_average:   Find average lightness of scene  
Invictus_threshold: Find relatively bright objects  
Invictus_blur_v_h:  Create halo around said bright objects  
Invictus_night:     Desaturate, add moonlight, add bloom  
Invictus_day:       RGB curves on Diffuse  
Invictus_composite: Composite night, day and bloom using average  


Invictus_fog:       no z-buffer to work with, cannot be used  
Invictus_blur:      n^2 complexity, inefficient, not needed  
Invictus_convolution:   no real application, but a cool kernel implementation  
