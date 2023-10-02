# 📷 Sirosky's Super Resolution Models

A repository containing upscaling models I created for public use. Currently, there are only 2x models for anime, but I plan on training models for RL footage at some point as well. The easiest ways to use these models would be through [Chainner](https://chainner.app/) (slower, but free) or [Enhancr](https://github.com/mafiosnik777/enhancr) (faster, but freemium). See [How to Upscale a Video Using chaiNNer (Step by Step)](https://github.com/Sirosky/Upscale-Hub/wiki/%F0%9F%93%BA-How-to-Upscale-a-Video-Using-chaiNNer-(Step-by-Step)) and the [enhancr wiki](https://github.com/mafiosnik777/enhancr/wiki) on how to get started with upscaling.

![Simple_Image_Compare_1 1_2bN7HYvgqP](https://github.com/Sirosky/Sirosky-Upscaling-Models/assets/2752448/08daf2a6-5325-42ee-a29b-dcfcd665d735)

*Comparison image for [REDACTED].*

# ⏬ Released Models
*Ratings included for each model are meant to serve as a quick point of reference to see how the models differ.*
### **HD/FHD Sources - Ani4K \[Gen 5, Compact\]**

\[Gen 5, Compact\] As the name suggests, Ani4K is trained to create natural-looking 2K/4K upscales from 720p/1080p sources. In particular, the model has superb detail retention.

- **[Download](https://github.com/Sirosky/Upscale-Hub/releases/tag/compact)**
- **Image Comparisons**:
    - [Blur Comparison](https://imgsli.com/MTg2NTg5/4/5)
    - [General Comparison](https://imgsli.com/MTg2ODI2)
- **Detail Retention**: ⭐⭐⭐⭐⭐
- **Compression Cleanup**: ⭐⭐(will deal with compression in HD/FHD BD and WEB sources without a hitch, but may be less suited for DVDs-- I'll be releasing separate models for DVDs)

### **Legacy Model - AniScaleV1 \[Gen 1, Compact\]**

My very first publicly released model. I consider it obsolete at this point, but some people might prefer the sharper look, so I'm releasing it here as well. As a first generation model, I trained AniScale to serve as a general-purpose model for all sources. Unfortunately, it simply isn't possible to have a single model do everything well-- subsequent generations of models are more specialized, and will do better for the sources they specialize in. While the model is great with details and dealing with a variety of video artifacts, it has a tendency to oversharpen some sources and background details. It doesn't handle blur at all either, though that's a problem common with many other anime models.

- **[Download](https://github.com/Sirosky/Upscale-Hub/blob/main/2x_AniScaleV1_55000.pth)**
- **Image Comparison**
- **Detail Retention**: ⭐⭐⭐⭐
- **Compression Cleanup**: ⭐⭐⭐⭐
- **Blur / DOF Effect Retention**: ⭐ (oversharpens out-of-focus objects)
- **Upscaling Artifacts**: ⭐⭐⭐ (slight color shifting on some objects)

# 🤝 Tools Utilized and Acknowledgements

- [ChaiNNer](https://chainner.app/) by Joey and contributors: The backbone of any of my bulk image processing and upscaling process. These models would not be possible without ChaiNNer.
- [ImgAlign](https://github.com/sonic41592/ImgAlign) by sonic41592: A fantastic little tool which can automate one of those tedious parts of image pair dataset preparation.
- [Image Pearer](https://github.com/Sirosky/Image-Pearer): A tool to automate the image pairing process by yours truly. Allows automation of the _other_ most tedious part of the image pair dataset preparation process.
- [OpenModelDB](https://openmodeldb.info/): A fantastic resource for all things upscaling.
- [TraiNNer Redux and Forks](https://github.com/joeyballentine/traiNNer-redux) by Joey, muslll and other contributors: All my models are trained on Redux and its forks.
- [Dataset Destroyer](https://github.com/Kim2091/helpful-scripts/tree/main/Dataset%20Destroyer) by Kim2091: A crucial part of the dataset preparation process that makes image degradation oh so easy!
- The developers and contributors to neural network models such as [ESRGAN]([url](https://github.com/xinntao/ESRGAN)), [SRVGGNetCompact]([url](https://github.com/xinntao/Real-ESRGAN)), [OmniSR](https://github.com/Francis0625/Omni-SR), [SwinIR]([url](https://github.com/JingyunLiang/SwinIR)) and more for developing the networks on which these models are based.
- [Simple Image Compare](https://github.com/Sirosky/Simple-Image-Compare): Another tool by yours truly. A minimalistic image comparison tool which I developed because ICAT sucks.
- And last but certainly not least, the [Enhance Everything Discord community](https://discord.gg/cpAUpDK) for their invaluable support and guidance. I also blame them for my neural network training addiction.


