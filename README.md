# Object Tracking with OpenCV

A Jupyter notebook ([`sample.ipynb`](sample.ipynb)) that tracks a race car through a video using
OpenCV's single-object trackers (CSRT, KCF, MIL, legacy trackers and the deep-learning trackers),
writes an annotated video and plays it back inline. Adapted from OpenCV Bootcamp notebook 11 and
updated for OpenCV 4.10+ / 5.x and NumPy 2.x.

## Setup

```bash
git clone https://github.com/arhyneRWU/ObjectTrackingDemo.git
cd ObjectTrackingDemo
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Use `opencv-contrib-python`, not `opencv-python`. The two conflict, so don't install both.
For inline video playback, install `ffmpeg` too (`brew install ffmpeg` on macOS).

## Running

Open `sample.ipynb` in Jupyter or PyCharm and run all cells. The first run downloads the sample
video (about 400 MB, including the GOTURN model files) into `data/`. Annotated videos are written to `outputs/`.

To try a different tracker, change `TRACKER_TYPE` in the Configuration cell. The NANO, VIT and
DASIAMRPN trackers need their `.onnx` model files in `models/`.

## Layout

| Path | Contents |
|---|---|
| `sample.ipynb` | The notebook |
| `data/` | Downloaded video assets (not committed) |
| `models/` | Model files for the deep-learning trackers (not committed) |
| `outputs/` | Generated videos (not committed) |
