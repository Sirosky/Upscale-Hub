<p align="center">
  <img src="https://github.com/Sirosky/Upscale-Hub/assets/2752448/a36d9d0a-e975-48ef-8281-003ad4a84c7f"/>
</p>
<p align="center">
Upscale Hub: a repository of resources for upscaling and neural network training, as well as a collection of the models I've trained.
</p>

******

<p align="center">
  <img src="https://github-production-user-asset-6210df.s3.amazonaws.com/2752448/271466226-08daf2a6-5325-42ee-a29b-dcfcd665d735.gif" alt="animated" />
</p>
<p align="center">
  <i>Comparison image for AniScale 2 (WIP).</i>
</p>

# ✨ How to Upscale

Upscaling is easiest done through:

- [chaiNNer](https://chainner.app/) (slower, but free); or
- [enhancr](https://github.com/mafiosnik777/enhancr) (faster, but freemium).

See [How to Upscale a Video Using chaiNNer (Step by Step)](https://github.com/Sirosky/Upscale-Hub/wiki/%F0%9F%93%BA-How-to-Upscale-a-Video-Using-chaiNNer-(Step-by-Step)) and the [enhancr wiki](https://github.com/mafiosnik777/enhancr/wiki) on how to get started with upscaling. Both are great starting points, but if you're not sure which one to pick, check [out the comparison here](https://github.com/Sirosky/Upscale-Hub/wiki/%F0%9F%A4%94-Picking-Between-chaiNNer-and-enhancr).

# 📈 How to Train Your Own Model

If you're looking for a guide on how to train your own model, check out the following:

- [Training a Model in neosr](https://github.com/Sirosky/Upscale-Hub/wiki/%F0%9F%93%88-Training-a-Model-in-NeoSR)- A guide I wrote which is up-to-date with current training methodologies, and my totally unbiased personal takes.
- [Training an image upscaling model](https://www.youtube.com/watch?v=iH7-eYlf7eg)- For those that prefer the video format. I recommend using neosr, but much of the information is still applicable.
- [Additional resources for training](https://github.com/Kim2091/training-info) - A list of additional resources and other information for training purposes, prepared by Kim2091.

# ⏬ Released Models
*Ratings included for each model are meant to serve as a quick point of reference to see how the models differ.*

### **DVD/HD/FHD Sources - AniScale 2 \[Gen 6, OmniSR and Compact\]**

\[Gen 6, OmniSR and Compact\] The successor and replacement to the original AniScale, and a substantial upgrade in nearly every respect. AniScale 2 is a versatile and faithful anime model trained for use on a variety of post ~2000 sources. Superb blur and depth of field handling, thorough WEB and DVD compression repair, and pleasing line art refinement are the hallmarks of AniScale 2.

- While AniScale 2 is trained first and foremost as an OmniSR model, AniScale 2 is also intended to be a platform to explore multiple SISR archs. For starters, I've trained OmniSR and Compact versions, but more will come.
- AniScale 2 also comes with a "refiner" model, creatively named AniScale 2 Refiner (AS2R). AS2R is a 1x Compact model (for maximum speed) trained to supplement and increase the versatility of AniScale 2, without making the base model excessively aggressive. The Refiner is focused on providing light sharpening, fixing line art and line thinning, depending on whether you run the model before or after upscaling with AniScale 2. 
- For more information, please visit the [Github wiki page](https://github.com/Sirosky/Upscale-Hub/wiki/%F0%9F%8C%9F-AniScale-2-&--AniScale-2-Refiner).

- **[Download](https://github.com/Sirosky/Upscale-Hub/releases/tag/AniScale2)**
- **Image Comparisons**:
    - [Blur Comparison](https://imgsli.com/MjEyMjQ1/5/4)
    - [General Comparison](https://imgsli.com/MjEyMjQw/0/1)
- **Detail Retention**: ⭐⭐⭐⭐
- **Compression Cleanup**: ⭐⭐⭐⭐⭐
- 
### **HD/FHD Sources - Ani4K \[Gen 5, Compact\]**

\[Gen 5, Compact\] As the name suggests, Ani4K is trained to create natural-looking 2K/4K upscales from 720p/1080p sources. In particular, the model has superb detail retention.

- **[Download](https://github.com/Sirosky/Upscale-Hub/releases/tag/Ani4K)**
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

- [chaiNNer](https://chainner.app/) by Joey and contributors: The backbone of any of my bulk image processing and upscaling process. These models would not be possible without ChaiNNer.
- [ImgAlign](https://github.com/sonic41592/ImgAlign) by sonic41592: A fantastic little tool which can automate one of those tedious parts of image pair dataset preparation.
- [Image Pearer](https://github.com/Sirosky/Image-Pearer): A tool to automate the image pairing process by yours truly. Allows automation of the _other_ most tedious part of the image pair dataset preparation process.
- [OpenModelDB](https://openmodeldb.info/): A fantastic resource for all things upscaling.
- [neosr](https://github.com/muslll/neosr) by muslll: The hottest new training platform!
- [TraiNNer Redux and Forks](https://github.com/joeyballentine/traiNNer-redux) by Joey, muslll and other contributors. While I've largely moved over to neosr, I've spent a LOT of time on Redux.
- [Dataset Destroyer](https://github.com/Kim2091/helpful-scripts/tree/main/Dataset%20Destroyer) by Kim2091: A crucial part of the dataset preparation process that makes image degradation oh so easy!
- The developers and contributors to neural network models such as [ESRGAN]([url](https://github.com/xinntao/ESRGAN)), [SRVGGNetCompact]([url](https://github.com/xinntao/Real-ESRGAN)), [OmniSR](https://github.com/Francis0625/Omni-SR), [SwinIR]([url](https://github.com/JingyunLiang/SwinIR)) and more for developing the networks on which these models are based.
- [Simple Image Compare](https://github.com/Sirosky/Simple-Image-Compare): Another tool by yours truly. A minimalistic image comparison tool which I developed because ICAT sucks.
- And last but certainly not least, the [Enhance Everything Discord community](https://discord.gg/cpAUpDK) for their invaluable support and guidance. I also blame them for my neural network training addiction.


