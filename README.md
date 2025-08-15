<div align="center">

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



<a><img src="assets/teaser.gif" alt="S²-Guidance Teaser Image" width="90%">

</div>



<a href='https://arxiv.org/abs/2503.18942'><img src='https://img.shields.io/badge/arXiv-2503.18942-b31b1b.svg'></a> &nbsp;&nbsp;&nbsp;&nbsp;
<a href='https://liuff19.github.io/Video-T1/'><img src='https://s2guidance.github.io/'></a> &nbsp;&nbsp;&nbsp;&nbsp;
<a href='https://mp.weixin.qq.com/s/HtJHXGgTAhi-uBWSsgqOKQ'><img src='https://img.shields.io/badge/%E5%BE%AE%E4%BF%A1-%E4%B8%AD%E6%96%87%E4%BB%8B%E7%BB%8D-green'></a> &nbsp;&nbsp;&nbsp;&nbsp;
![Teaser Visualization](assets/teaser.png)











## 🔥 Updates
- **[2025/08]** Our paper is available on [arXiv](https://arxiv.org/abs/2312.01323) and the [project page](https://chubin-chen.github.io/S2-Guidance/) is live!
- **[Coming Soon]** Code models will be released soon.

##  Showcase
Here are some examples comparing the results from standard Classifier-Free Guidance (CFG) with our **S²-Guidance**. Our method consistently produces higher-fidelity and more coherent results for both images and videos.

**Prompt:** "A floating castle above the clouds, with 'S² Guidance Is All You Need' swirling in the mist."
| CFG (Baseline) | Ours (S²-Guidance) |
|:--------------:|:------------------:|
| <img src="assets/baseline2.jpg" alt="CFG result for floating castle"> | <img src="assets/ours2.jpg" alt="Our result for floating castle"> |

---

**Prompt:** "A woman is holding a bouquet of balloons and celebrating a birthday."
| CFG (Baseline) | Ours (S²-Guidance) |
|:--------------:|:------------------:|
| <img src="assets/baseline3.jpg" alt="CFG result for balloons"> | <img src="assets/ours3.jpg" alt="Our result for balloons"> |

---

**Prompt:** "A red book and an ivory sheep."
| CFG (Baseline) | Ours (S²-Guidance) |
|:--------------:|:------------------:|
| <img src="assets/baseline4.jpg" alt="CFG result for red book"> | <img src="assets/ours4.jpg" alt="Our result for red book"> |

---

**Prompt:** "A breathtaking close-up of a woman frozen in time as golden threads of light weave around her face..."
| CFG (Baseline) | Ours (S²-Guidance) |
|:--------------:|:------------------:|
| <video src="assets/baseline_video1.mp4" autoplay loop muted playsinline alt="CFG video for golden threads"></video> | <video src="assets/ours_video1.mp4" autoplay loop muted playsinline alt="Our video for golden threads"></video> |

---

**Prompt:** "An astronaut flying in space, zoom out."
| CFG (Baseline) | Ours (S²-Guidance) |
|:--------------:|:------------------:|
| <video src="assets/baseline_video2.mp4" autoplay loop muted playsinline alt="CFG video for astronaut"></video> | <video src="assets/ours_video2.mp4" autoplay loop muted playsinline alt="Our video for astronaut"></video> |

<br>


## 📖 Abstract
> Classifier-free Guidance (CFG) is a widely used technique in modern diffusion models for enhancing sample quality and prompt adherence. However, through an empirical analysis on Gaussian mixture modeling with a closed-form solution, we observe a discrepancy between the suboptimal results produced by CFG and the ground truth. The model's excessive reliance on these suboptimal predictions often leads to semantic incoherence and low-quality outputs. To address this issue, we first empirically demonstrate that the model's suboptimal predictions can be effectively refined using sub-networks of the model itself. Building on this insight, we propose **S²-Guidance**, a novel method that leverages stochastic block-dropping during the forward process to construct sub-networks, effectively guiding the model away from potential low-quality predictions and toward high-quality outputs. Extensive qualitative and quantitative experiments on text-to-image and text-to-video generation tasks demonstrate that **S²-Guidance** delivers superior performance, consistently surpassing CFG and other advanced guidance strategies.

## 🙏 Acknowledgements
This work is built upon many amazing open-source projects. We would like to thank the developers of [Diffusers](https://github.com/huggingface/diffusers), [PyTorch](https://pytorch.org/), and other related libraries for their contributions to the community.

