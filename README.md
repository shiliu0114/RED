# RED: Residual Estimation Diffusion for Low-Dose PET Sinogram Reconstruction
[![arXiv](https://img.shields.io/badge/arXiv-2411.05354-b31b1b.svg)](https://arxiv.org/abs/2411.05354)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
This repository contains the PyTorch implementation of the paper **"RED: Residual Estimation Diffusion for Low-Dose PET Sinogram Reconstruction"**.
> **Code Availability:** The source code is available at [https://github.com/yqx7150/RED](https://github.com/yqx7150/RED).

## Abstract
Recent advances in diffusion models have demonstrated exceptional performance in generative tasks across various fields. In positron emission tomography (PET), the reduction in tracer dose leads to information loss in sinograms. Using diffusion models to reconstruct missing information can improve imaging quality. Traditional diffusion models effectively use Gaussian noise for image reconstructions. However, in low-dose PET reconstruction, Gaussian noise can worsen the already sparse data by introducing artifacts and inconsistencies. To address this issue, we propose a diffusion model named residual estimation diffusion (RED). From the perspective of diffusion mechanism, RED uses the residual between sinograms to replace Gaussian noise in diffusion process, respectively sets the low-dose and full-dose sinograms as the starting point and endpoint of reconstruction. This mechanism helps preserve the original information in the low-dose sinogram, thereby enhancing reconstruction reliability. From the perspective of data consistency, RED introduces a drift correction strategy to reduce accumulated prediction errors during the reverse process. Calibrating the intermediate results of reverse iterations helps maintain the data consistency and enhances the stability of reconstruction process. Experimental results show that RED effectively improves the quality of low-dose sinograms as well as the reconstruction results. 

## Method Overview

<p align="center">
  <img src="assets/drift_correction.png" alt="Drift Correction Strategy" width="600">
  <br>
  <em>Figure 2: Visualization of the drift correction effect during the sampling trajectory.</em>
</p>




## Citation
```bibtex
If you use this code or find our work useful, please cite:
@article{ai2024red,
  title={RED: Residual Estimation Diffusion for Low-Dose PET Sinogram Reconstruction},
  author={Ai, Xingyu and Huang, Bin and Chen, Fang and Shi, Liu and Li, Binxuan and Wang, Shaoyu and Liu, Qiegen},
  journal={arXiv preprint arXiv:2411.05354},
  year={2024}
}
