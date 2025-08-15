# S²-Guidance: Stochastic Self-Guidance for Training-Free Enhancement of Diffusion Models

<p align="center">
  <!-- 作者行 -->
  Chubin Chen<sup>1,2</sup>,
  Jiashu Zhu<sup>2</sup>,
  Xiaokun Feng<sup>2,3</sup>,
  Nisha Huang<sup>1</sup>
  <br>
  Meiqi Wu<sup>2,3</sup>,
  Fangyuan Mao<sup>2</sup>,
  Jiahong Wu<sup>2,‡</sup>,
  Xiangxiang Chu<sup>2</sup>,
  Xiu Li<sup>1,†</sup>
  <br><br>
  <!-- 机构行 -->
  <sup>1</sup>Tsinghua University &nbsp;&nbsp;&nbsp;
  <sup>2</sup>AMAP, Alibaba Group &nbsp;&nbsp;&nbsp;
  <sup>3</sup>CASIA
  <br>
  <sup>†</sup>Corresponding author. &nbsp;&nbsp;&nbsp;
  <sup>‡</sup>Project lead.
</p>


</div>

<!-- 徽章 (Badges) 部分 (已修正，移除了下划线) -->
<p align="center">
  <a href="https://arxiv.org/abs/2312.01323" style="text-decoration: none;">
    <img src="https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white" alt="Paper"/>
  </a>
  &nbsp;&nbsp;&nbsp;
  <a href="https://s2guidance.github.io/" style="text-decoration: none;">
    <img src="https://img.shields.io/badge/Project-Page-blue?logo=googlechrome&logoColor=white" alt="Project Page"/>
  </a>
  &nbsp;&nbsp;&nbsp;
</p>



<!-- Teaser Image -->
<img src="assets/teaser.jpg" alt="S²-Guidance Teaser Image" width="100%">

## 🔥 Updates
- **[2025/08]** Our paper is available on [arXiv](https://arxiv.org/abs/2312.01323) and the [project page](https://s2guidance.github.io/) is live!
- **[Coming Soon]** Code will be released. 


## 📣 Overview

<p align="center">
  <img src="assets/method_v3.jpg" alt="Method Overview Diagram" width="100%">
</p>

We propose **S²-Guidance**, a novel method that leverages stochastic block-dropping during the forward process to construct sub-networks, effectively guiding the model away from potential low-quality predictions and toward high-quality outputs. Extensive qualitative and quantitative experiments on text-to-image and text-to-video generation tasks demonstrate that **S²-Guidance** delivers superior performance, consistently surpassing CFG and other advanced guidance strategies.


## 🎉 Results
Here are some examples comparing the results from standard Classifier-free Guidance (CFG) with our **S²-Guidance**. Our method consistently produces higher-fidelity and more coherent results.

### Text-to-Image Generation

**Prompt:** "The bold dramatic strokes of the painter's brush created a stunning abstract masterpiece a work of emotional depth and intensity."
| CFG | Ours (S²-Guidance) |
|:--------------:|:------------------:|
| <img src="assets/baseline1.jpg" alt="CFG Image 1"> | <img src="assets/ours1.jpg" alt="Ours Image 1"> |

---

**Prompt:** "A floating castle above the clouds, with 'S² Guidance Is All You Need' swirling in the mist."
| CFG | Ours (S²-Guidance) |
|:--------------:|:------------------:|
| <img src="assets/baseline2.jpg" alt="CFG Image 2"> | <img src="assets/ours2.jpg" alt="Ours Image 2"> |

---

**Prompt:** "A woman is holding a bouquet of balloons and celebrating a birthday."
| CFG | Ours (S²-Guidance) |
|:--------------:|:------------------:|
| <img src="assets/baseline3.jpg" alt="CFG Image 3"> | <img src="assets/ours3.jpg" alt="Ours Image 3"> |

---

**Prompt:** "A red book and an ivory sheep."
| CFG | Ours (S²-Guidance) |
|:--------------:|:------------------:|
| <img src="assets/baseline4.jpg" alt="CFG Image 4"> | <img src="assets/ours4.jpg" alt="Ours Image 4"> |

---

**Prompt:** "A cat sitting besides a rocket on a planet with a lot of cactuses."
| CFG | Ours (S²-Guidance) |
|:--------------:|:------------------:|
| <img src="assets/baseline5.jpg" alt="CFG Image 5"> | <img src="assets/ours5.jpg" alt="Ours Image 5"> |

---

**Prompt:** "A woman sitting under an umbrella in the middle of a restaurant."
| CFG | Ours (S²-Guidance) |
|:--------------:|:------------------:|
| <img src="assets/baseline6.jpg" alt="CFG Image 6"> | <img src="assets/ours6.jpg" alt="Ours Image 6"> |

### Text-to-Video Generation

**Prompt:** "A breathtaking close-up of a woman frozen in time as golden threads of light weave around her face, creating dynamic flowing patterns of energy amidst glowing particles."
<table border="0" style="width: 100%; text-align: center; margin-top: 20px;">
  <tr>
    <td style="text-align: center;">
      <b>CFG</b>
      <br>
      <video src="https://github.com/user-attachments/assets/ca181aed-1889-4b90-a885-ef429dc861e0" width="100%" controls autoplay loop muted playsinline alt="CFG Video 4"></video>
    </td>
    <td style="text-align: center;">
      <b>Ours (S²-Guidance)</b>
      <br>
      <video src="https://github.com/user-attachments/assets/b14c92be-860a-4596-91f3-ed8ce4e0e9cd" width="100%" controls autoplay loop muted playsinline alt="Ours Video 4"></video>
    </td>
  </tr>
</table>


---

**Prompt:** "An astronaut flying in space, zoom out."
<table border="0" style="width: 100%; text-align: center; margin-top: 20px;">
  <tr>
    <td style="text-align: center;">
      <b>CFG</b>
      <br>
      <video src="https://github.com/user-attachments/assets/255444a3-3130-4747-913c-fc9ad3e11ae8" width="100%" controls autoplay loop muted playsinline alt="CFG Video 3"></video>
    </td>
    <td style="text-align: center;">
      <b>Ours (S²-Guidance)</b>
      <br>
      <video src="https://github.com/user-attachments/assets/067fba6c-c244-4f6a-a55f-5ba785ad6264" width="100%" controls autoplay loop muted playsinline alt="Ours Video 3"></video>
    </td>
  </tr>
</table>

---

**Prompt:** "A car accelerating to gain speed."
<table border="0" style="width: 100%; text-align: center; margin-top: 20px;">
  <tr>
    <td style="text-align: center;">
      <b>CFG</b>
      <br>
      <video src="https://github.com/user-attachments/assets/8b1903e6-d45c-4411-81f7-4d93a008c427" width="100%" controls autoplay loop muted playsinline alt="CFG Video 2"></video>
    </td>
    <td style="text-align: center;">
      <b>Ours (S²-Guidance)</b>
      <br>
      <video src="https://github.com/user-attachments/assets/0886e3a1-e60e-49b3-9b7a-8b300820892d" width="100%" controls autoplay loop muted playsinline alt="Ours Video 2"></video>
    </td>
  </tr>
</table>

---

**Prompt:** "A parking meter and a truck."
<table border="0" style="width: 100%; text-align: center; margin-top: 20px;">
  <tr>
    <td style="text-align: center;">
      <b>CFG</b>
      <br>
      <video src="https://github.com/user-attachments/assets/8a6faf1a-5641-4467-89b3-ac5c7b6e716d" width="100%" controls autoplay loop muted playsinline alt="CFG Video 1"></video>
    </td>
    <td style="text-align: center;">
      <b>Ours (S²-Guidance)</b>
      <br>
      <video src="https://github.com/user-attachments/assets/73e453a1-7470-4d2a-8d10-fab8b5a3a0ba" width="100%" controls autoplay loop muted playsinline alt="Ours Video 1"></video>
    </td>
  </tr>
</table>

### User Study
<img src="assets/userstudy.jpg" alt="Quantitative Results" width="100%">

### Quantitative Results

#### HPSV2.1 & T2I-ComBench
<img src="assets/comparison.png" alt="Quantitative Results" width="100%">

#### VBench
<img src="assets/comparison2.png" alt="Quantitative Results2" width="100%">


## 🙏 Acknowledgements
This work is built upon many amazing open-source projects. We would like to thank the developers of [Diffusers](https://github.com/huggingface/diffusers), [PyTorch](https://pytorch.org/), and other related libraries for their contributions to the community.

## 📜 Citation
If you find our work useful for your research, please consider citing our paper.
