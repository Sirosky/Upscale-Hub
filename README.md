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

- Want to upscale a video? [Take a look here](https://github.com/Sirosky/Upscale-Hub/wiki/%F0%9F%93%BA-How-to-Upscale-a-Video).
- Want to upscale an image or multiple images? [Take a look here](https://github.com/Sirosky/Upscale-Hub/wiki/%F0%9F%93%B7-How-to-Upscale-an-Image-or-Multiple-Images).

# 📈 How to Train Your Own Model

If you're looking for a guide on how to train your own model, check out the following:

- [Training a Model in neosr](https://github.com/Sirosky/Upscale-Hub/wiki/%F0%9F%93%88-Training-a-Model-in-NeoSR)- A guide I wrote which is up-to-date with current training methodologies, and my totally unbiased personal takes.
- [Training an image upscaling model](https://www.youtube.com/watch?v=iH7-eYlf7eg)- For those that prefer the video format. I recommend using neosr, but much of the information is still applicable.
- [Additional resources for training](https://github.com/Kim2091/training-info) - A list of additional resources and other information for training purposes, prepared by Kim2091.

# ⏬ Released Models
*Ratings included for each model are meant to serve as a quick point of reference to see how the models differ.*

### <img src="https://github.com/Sirosky/Upscale-Hub/assets/2752448/52c56a2c-d2d0-487a-a201-c991dc2b0a06" width="64"/> **DVD/HD/FHD Sources - AniScale 2 \[Gen 6, OmniSR, Compact, etc.\]**

\[Gen 6, OmniSR, Compact, etc.\] The successor and replacement to the original AniScale, and a substantial upgrade in nearly every respect. AniScale 2 is a versatile and faithful anime model trained for use on a variety of post ~2000 sources. Superb blur and depth of field handling, thorough WEB and DVD compression repair, and pleasing line art refinement are the hallmarks of AniScale 2.

- While AniScale 2 is trained first and foremost as an OmniSR model, AniScale 2 is also intended to be a platform to explore multiple SISR archs. For starters, I've trained OmniSR and Compact versions, but more will come.
- AniScale 2 also comes with a "refiner" model, creatively named AniScale 2 Refiner (AS2R). AS2R is a 1x Compact model (for maximum speed) trained to supplement and increase the versatility of AniScale 2, without making the base model excessively aggressive. The Refiner is focused on providing light sharpening, fixing line art and line thinning, depending on whether you run the model before or after upscaling with AniScale 2. 
- For more information, please visit the [Github wiki page](https://github.com/Sirosky/Upscale-Hub/wiki/%F0%9F%8C%9F-AniScale-2-&--AniScale-2-Refiner).

- **[Download](https://github.com/Sirosky/Upscale-Hub/releases/tag/AniScale2)**
    - If you're unsure which version to start with, I recommend trying the [OmniSR version](https://github.com/Sirosky/Upscale-Hub/releases/download/AniScale2/2x_AniScale2_Omni_i16_40K.pth) first. More details on the Wiki page linked above.
- **Image Comparisons**:
    - [Blur Comparison](https://imgsli.com/MjEyMjQ1/5/4)
    - [General Comparison](https://imgsli.com/MjEyMjQw/0/1)
- **Detail Retention**: ⭐⭐⭐⭐
- **Compression Cleanup**: ⭐⭐⭐⭐⭐

### <img src="https://github.com/Sirosky/Upscale-Hub/assets/2752448/978362f6-540b-424b-9e76-55432c5cea3a" width="64"/> **HD/FHD Live Action TV and Cinema - Open Proteus \[Compact\]**

\[Compact\] Yes... not an anime model for a change! Topaz Video AI is generally considered amongst the industry leaders of in upscaling movies and TV, however it sits behind a significant paywall. Open Proteus is a free alternative to Topaz's Proteus AI, and intended to upscale high-quality and low-noise HD sources to 4K. While I won't claim this is superior to Topaz Proteus by most metrics (which would be a near-impossible feat on open-source architectures anyway), Open Proteus produces output which is highly faithful, without causing oversharpening or upscaling artifacts.

- **[Download](https://github.com/Sirosky/Upscale-Hub/releases/tag/AniScale2](https://github.com/Sirosky/Upscale-Hub/releases/tag/OpenProteus))**
- **Image Comparisons**: [General Comparison](https://slow.pics/c/NM9BzYz0)
  
### **Legacy Models**
![Banner AniScale 2](https://github.com/Sirosky/Upscale-Hub/assets/2752448/2d974639-9d25-439c-b75e-52b31285d1df)


Looking for one of my older models? You can [still find them here](https://github.com/Sirosky/Upscale-Hub/blob/main/Legacy/Legacy%20Models.md).

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


