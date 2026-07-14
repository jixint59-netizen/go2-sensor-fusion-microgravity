# GO2 Sensor Fusion and Material Recognition in MuJoCo

Simulation code developed for a University of Manchester MSc Robotics dissertation project.

## Uploaded code

The current source package is stored at:

- `projects/go2_floor_material_recognition_v2_1_source.tar.gz`

It contains the GO2 four-material-floor simulation, gait controller, foot-contact sensing, live material-recognition dashboard, tests, launch scripts and MuJoCo XML files.

Large GO2 OBJ mesh assets are not duplicated in this repository. After extracting the source package, run:

```bash
bash scripts/fetch_go2_assets.sh
```

This downloads the official Unitree GO2 assets from Google DeepMind MuJoCo Menagerie.

## Quick start

```bash
git clone https://github.com/jixint59-netizen/go2-sensor-fusion-microgravity.git
cd go2-sensor-fusion-microgravity
mkdir -p projects
tar -xzf projects/go2_floor_material_recognition_v2_1_source.tar.gz -C .
cd projects/go2_floor_material_recognition_v2_1
bash scripts/fetch_go2_assets.sh
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
./verify_project.sh
./start_material_walk_demo.sh
```

## Research status

The locomotion and visualisation pipelines are operational. The four-material classifier is an experimental simulation baseline and still requires calibration and quantitative validation before being reported as a final dissertation result.

## Dissertation files

The `thesis/` directory contains folders for chapters, figures, experiments and references.
