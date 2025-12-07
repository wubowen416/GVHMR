# GVHMR: World-Grounded Human Motion Recovery via Gravity-View Coordinates
Adapted to windows and output estimated parameters as a json file.

## Setup
### Windows
Please see [installation](docs/INSTALL_win.md) for details.

### Demo
Demo entries are provided in `tools/demo`.

```shell
python tools/demo/demo.py --video=docs/example_video/tennis.mp4 -s
```
- `-s` is used to skip visual odometry if you know the camera is static, otherwise the camera will be estimated by DPVO (unsupported currently).
