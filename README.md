# Sirosky's Super Resolution Models

A repository containing upscaling models I created for public use. Currently, there are only 2x models for anime, but I plan on training models for RL footage at some point as well.

If you are just looking for the sharpest possible upscaling model, my models probably won't be of interest. But if you're looking for models trained with a focus on the faithful enhancement of the video and images being upscaled, then have a gander.

# Released Models

- **Upscaling HD/FHD**
    - **2x Ani4K** \[Gen 5, Compact\]: As the name suggests, Ani4K is trained to create natural-looking 2K/4K upscales from 720p/1080p sources (that is, the results should look as close as possible to a hypothetical native 2K/4K release from a studio). To achieve this, particular attention was placed on:
        - **Depth of Field and Intentional Blur Retention**: DOF/blur effects are extremely common in modern anime. While it can be tempting to sharpen the crap out of everything on the screen (see AniScaleV1 below), such an approach can create odd-looking results when it brings into focus items that should be out of focus. Ani4K's DOF/blur effect retention isn't perfect, but it gets pretty close.
        - **Line Art Retention**: Retaining crisp line art is key to making anime upscales look pleasing to the eye. Some models, even those trained on modern anime, can produce "hallowed" lines at higher resolutions. Ani4K avoids this issue by "solidifying" the lines.
        - **Compression Clean-up**: Even modern Bluray releases will contain some compression artifacts. Ani4K will clean up artifacting as part of the upscaling process.
        - **Detail Retention**: This largely speaks for itself-- you don't want a model that nukes textures and/or destroys details. Ani4K will retain complex textures and subtle details without a hitch.
- **Legacy Model**
    
    - **2x AniScaleV1** \[Gen 1, Compact\]: My very first publicly released model. I consider it obsolete at this point, but some people might prefer the sharper look, so I'm releasing it here as well. As a first generation model, I trained AniScale to serve as a general-purpose model for all sources. Unfortunately, it simply isn't possible to have a single model do everything well-- subsequent generations of models are more specialized, and suited will do better for specific sources.
        
        - *Strengths:* Great with details and dealing with all sorts of video artifacts-- dotcrawl, haloing, bleeding, etc. It will also deal with "hallowed" lines found in some older anime.
        - *Weaknesses:* Will oversharpen some sources. While the model is good with details, it might actually oversharpen some details. Background objects that aren't supposed to be in focus might be sharpened. Does NOT like blur at all, though to be fair, that is a problem with the majority of anime upscaling models out there. It will sometimes also color shift on smaller objects or lines.
