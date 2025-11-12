# Robust Tracking Module
Implementation of the Robust Tracking Module on SiamRPN

![RTM Module](Assets/RTM_diag.png)

## Pretrained model

[GDrive](https://drive.google.com/file/d/1TbQztkEbEp4wRAZl-z18U4lNxYn9gSp9/)

## Setup environment

```
conda env create -f environment.yaml
conda activate rtm
```

## Training

coming soon

## Run tracking

### Dataset evaluation
- Set correct paths for each dataset in ```configs/local.py```
- Download pretrained model and save in ```checkpoints/model_RTM.pth```
- ```python tracking_evaluation.py --dataset lasot --distortion original```

### Run demo
- Run on video: ```python demo.py path/to/video.mp4```
- Run on webcam: ```python demo.py 0```
- Distort input with ```--distortion``` argument:
    - White Gaussian Noise: ```WGN```
    - Salt and Pepper: ```SnP```
    - Gaussian Blur: ```GB```
- Select initial bounding box with mouse (click and drag)

## Citation

```
@article{karakostas2025enhancing,
  title={Enhancing visual object tracking robustness through a lightweight denoising module},
  author={Karakostas, Iason and Mygdalis, Vasileios and Nikolaidis, Nikos and Pitas, Ioannis},
  journal={The Visual Computer},
  pages={1--18},
  year={2025},
  publisher={Springer}
}
```

## Related repositories
- [DaSiamRPN](https://github.com/foolwood/DaSiamRPN)
- [Siamese-RPN-pytorch](https://github.com/songdejia/Siamese-RPN-pytorch)
- [SiamRPN Pytorch](https://github.com/huanglianghua/siamrpn-pytorch)
- [GOT-10k toolkit](https://github.com/got-10k/toolkit)

## Acknowledgement
This work has received funding from European Union’s Horizon 2020 research and innovation programme under grant agreement No 871479 (AERIAL-CORE), and the research project “Energy Efficient and Trustworthy Deep Learning-DeepLET” implemented in the framework of H.F.R.I call “Basic research Financing (Horizontal support of all Sciences)” under the National Recovery and Resilience Plan “Greece 2.0” funded by the European Union-NextGenerationEU (Pr. Number: 016762).
