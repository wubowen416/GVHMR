# Install

## Environment

```bash
git clone https://github.com/wubowen416/GVHMR
cd GVHMR

python3.10 -m venv .venv
.venv\Scripts\activate.bat
pip install chumpy --no-build-isolation
pip install "git+https://github.com/samson-wang/cython_bbox.git#egg=cython-bbox"
pip install -r requirements_win.txt
pip install -e .
```

## Checkpoint files
Download checkpoints from [this url](https://drive.google.com/file/d/1_5PvDYrxVfOxVqVlwzKiwPPHLpgcaVH3/view?usp=sharing).
Unzip files to `.\inputs` to have the following order:

```bash
inputs/checkpoints/
├── body_models/smplx/
│   └── SMPLX_NEUTRAL.npz # SMPLX (We predict SMPLX params + evaluation)
├── body_models/smpl/
│   └── SMPL_NEUTRAL.pkl  # SMPL (rendering and evaluation)
├── dpvo/
│   └── dpvo.pth
├── gvhmr/
│   └── gvhmr_siga24_release.ckpt
├── hmr2/
│   └── epoch=10-step=25000.ckpt
├── vitpose/
│   └── vitpose-h-multi-coco.pth
└── yolo/
    └── yolov8x.pt
```