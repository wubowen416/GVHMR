# GVHMR: World-Grounded Human Motion Recovery via Gravity-View Coordinates
Adapted to windows and output estimated parameters as a json file.

## Setup
### Windows
Please see [installation](docs/INSTALL_win.md) for details.

## Usage
```bash
# Example
python tools/demo/demo_ct.py --video docs/example_video/avita/BridgeClip_SMPLXAngle4FaceA_0120.mp4 --output_root outputs -s
```
- `--video`: Path to your video.
- `-s`: skip visual odometry if you know the camera is static, otherwise the camera will be estimated by DPVO (unsupported currently).

Results are saved to `$OUTPUT_ROOT\$VIDEO_NAME\hmr4d_results.json`. With the following keys:
- `frames`: estimated data for each frame, containing the following keys:
    - `body_pose`: smpl joint rotation parameters in axis-angle format.
    - `global_orient`: global orientation.
    - `transl`: translation.
    - `transl_rel`: relative `transl` to preivous frame.
    - `ct_transl`: camera coordinate system transformed `transl`. 
    - `ct_transl_rel`: relative `ct_transl` to preivous frame.
    - `ct_orient`: camera coordinate system transformed `global_orient`.
    - `frame_time`: timing of the current frame.
- `batas`: estimated body shape parameters.
