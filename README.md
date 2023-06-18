# 📷 Sirosky's Super Resolution Models

A repository containing upscaling models I created for public use. Currently, there are only 2x models for anime, but I plan on training models for RL footage at some point as well. The easiest ways to use these models would be through [Chainner](https://chainner.app/) (slower, but free) or [Enhancr](https://github.com/mafiosnik777/enhancr) (faster, but freemium).

![image](https://github.com/Sirosky/Sirosky-Upscaling-Models/assets/2752448/06777dde-eff7-4c88-b83b-a2602e090a5a)

*Comparison image for AniDVD.*

# ⏬ Released Models
*Ratings included for each model are meant to serve as a quick point of reference to see how the models differ.*
### **HD/FHD Sources - Ani4K \[Gen 5, Compact\]**

\[Gen 5, Compact\] As the name suggests, Ani4K is trained to create natural-looking 2K/4K upscales from 720p/1080p sources. In particular, the model has superb detail retention.

- **[Download](https://github.com/Sirosky/Sirosky-Upscaling-Models/releases)**
- **Image Comparisons**:
    - [Blur Comparison](https://imgsli.com/MTg2NTg5/4/5)
    - [General Comparison](https://imgsli.com/MTg2ODI2)
- **Detail Retention**: ⭐⭐⭐⭐⭐
- **Compression Cleanup**: ⭐⭐(will deal with compression in HD/FHD BD and WEB sources without a hitch, but may be less suited for DVDs-- I'll be releasing separate models for DVDs)

### **Legacy Model - AniScaleV1 \[Gen 1, Compact\]**

My very first publicly released model. I consider it obsolete at this point, but some people might prefer the sharper look, so I'm releasing it here as well. As a first generation model, I trained AniScale to serve as a general-purpose model for all sources. Unfortunately, it simply isn't possible to have a single model do everything well-- subsequent generations of models are more specialized, and will do better for the sources they specialize in. While the model is great with details and dealing with a variety of video artifacts, it has a tendency to oversharpen some sources and background details. It doesn't handle blur at all either, though that's a problem common with many other anime models.

- **[Download](https://github.com/Sirosky/Sirosky-Upscaling-Models/blob/main/2x_AniScaleV1_55000.pth)**
- **Image Comparison**
- **Detail Retention**: ⭐⭐⭐⭐
- **Compression Cleanup**: ⭐⭐⭐⭐
- **Blur / DOF Effect Retention**: ⭐ (oversharpens out-of-focus objects)
- **Upscaling Artifacts**: ⭐⭐⭐ (slight color shifting on some objects)

# 📚 Model Training Principles

This section provides an overview of the guiding principles I follow while training my models. It should give a sense of whether these are the right models for you, and what sets my models apart from others.

**Balanced** **Sharpness**: While my models deblur and sharpen the input, they aren't the sharpest ones available. This is intentional-- the models aim to produce a *natural-looking* upscale, as if the result was something natively produced by the studio. In addition, oversharpening tends to produce undesireable artifacts.

![image](https://github.com/Sirosky/Sirosky-Upscaling-Models/assets/2752448/d727a781-f4eb-40ea-902e-6e7164f76577)

*Roof tiles so sharp that you can cut yourself on them*.

**Line Art** **Retention**: Retaining crisp line art is key to making anime upscales look pleasing to the eye. Some models, even those trained on modern anime, can produce "hallowed" lines (example below) at higher resolutions. My models are trained to retain / enhance line art, and of course, avoid the hallowed line effect.

![image](https://github.com/Sirosky/Sirosky-Upscaling-Models/assets/2752448/f37fa3d1-a16e-4b80-97a7-894cd0766587)

*Note how the lines here don't seem solid. Sometimes, it's an artistic decision. But this example is the model not properly handling line art after oversharpening.* 🤢

**Detail Retention**: This largely speaks for itself-- you don't want a model that nukes textures and/or destroys details. While it's not always possible to achieve flawless detail retention (especially with models that have more-aggressive clean-up), detail retention is something that my models generally excel in.

![image](https://github.com/Sirosky/Sirosky-Upscaling-Models/assets/2752448/88704f91-6858-42b3-b71a-d8a8783fd8a3)

*Where did the fence go?*

**Compression Clean-up**: This is self-explanatory as well. When upscaling, the model should clean up compression artifacts present in the source (haloing, noise, chroma bleed, etc.) rather than upscale the artifacts along with the rest of the picture. However, it is also important to not go overboard, as doing so comes at the expense of detail retention.

![image](https://github.com/Sirosky/Sirosky-Upscaling-Models/assets/2752448/7e4ab630-e787-454a-a250-b35531ee2eec)![image](https://github.com/Sirosky/Sirosky-Upscaling-Models/assets/2752448/70db5ab4-8f03-4e15-8482-e8b0f970b9ee)


*On the left, an example of a model that upscaled but didn't fix the white haloing, vs. on the right, AniDVD which upscaled and cleaned haloing*.

**Depth of Field and Intentional Blur Retention**: DOF/blur effects are extremely common in modern anime, and present even in older anime. While it can be tempting to sharpen the crap out of everything on the screen (see AniScaleV1 below), such an approach can create odd-looking results when it brings into focus items that should be out of focus. Aside from AniScaleV1, which is the first model I ever released, all my models are trained to handle blur effects appropriately.

![image](https://github.com/Sirosky/Sirosky-Upscaling-Models/assets/2752448/f560bd4c-6f42-425e-87ed-33fa4c8275ca)![image](https://github.com/Sirosky/Sirosky-Upscaling-Models/assets/2752448/36d51e5d-193c-4923-a631-33d8a40a1727)

*Some things are better left blurred...*

**Upscaling Artifacts**: Some models produce upscaling artifacts-- blemishes on the image generated by the model during the upscaling process. These can vary from annoying to hardly noticeable, but in my book, it's best to avoid generating artifacts to begin with!

![image](https://github.com/Sirosky/Sirosky-Upscaling-Models/assets/2752448/00f24508-da8d-4b8e-80ce-49e7f50c5927)![image](https://github.com/Sirosky/Sirosky-Upscaling-Models/assets/2752448/774bcdf6-f016-4b4d-b306-8d82381f148a)

*An example of a fairly subtle artifact-- the white glow generated at the intersection of the two lines.*
