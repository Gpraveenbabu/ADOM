# ADOM
# ADOM: ADMM-Based Optimization for Destriping Remote Sensing Images

[![License](https://img.shields.io/badge/license-CC_BY--NC--ND_4.0-green)](https://creativecommons.org/licenses/by-nc-nd/4.0/)
[![DOI](https://img.shields.io/badge/DOI-10.1109%2FACCESS.2023.3319268-blue)](https://doi.org/10.1109/ACCESS.2023.3319268)

ADOM is an *Alternating Direction Method of Multipliers (ADMM)-based optimization model* for removing stripe noise from remote sensing images, published in IEEE Access. It outperforms existing methods by combining:

✔ *Weight-based detection* (preserves image details)  
✔ *ADMM acceleration* (faster convergence)  
✔ *No training data required* (unlike deep learning approaches)  

---

## Key Features
- *Effective stripe removal* for both periodic and non-periodic noise  
- *Detail preservation* using adaptive weighted norms  
- *Computationally efficient* with momentum-based optimization  
- Validated on *simulated and real-world datasets* (Cuprite, Hyperion, MODIS)  

---

## Performance Highlights
| Metric        | Noisy Image | ADOM      | Improvement |
|---------------|-------------|-----------|-------------|
| PSNR (dB)     | 25.10       | *54.91* | +29.81      |
| SSIM          | 0.40        | *0.997* | +0.597      |
| Runtime (s)*  | -           | *0.52*  | Faster than RBS, GDF |  

*Tested on 256×256 Hyperion image (Intel i5-7600 @ 3.50GHz)  

---

## How It Works
1. *Optimization Formulation*:  
   - Minimizes stripe components via L₁ and weighted L₂,₁ norms  
   - Uses ADMM to split problem into efficient subproblems  

2. *Innovative Strategies*:  
   - *Weight Control*: Adjusts norms using residual parameters  
   - *Momentum Acceleration*: Speeds up convergence via Nesterov's method  

---

## Getting the Paper
Download the full manuscript:  
🔗 [IEEE Xplore](https://ieeexplore.ieee.org/document/10245689)  

---

## Citation
```bibtex
@article{kim2023adom,
  title={ADOM: ADMM-Based Optimization Model for Stripe Noise Removal in Remote Sensing Image}, 
  author={Kim, Namwon and Han, Seong-Soo and Jeong, Chang-Sung},
  journal={IEEE Access},
  year={2023},
  volume={11},
  pages={106587-106606},
  doi={10.1109/ACCESS.2023.3319268}
}
