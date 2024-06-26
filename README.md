# TrackNet-SoccerBall

TrackNet-SoccerBall is a project for tracking the soccer ball in a soccer match using the TrackNet model. This project leverages the TrackNetV3 model to accomplish ball tracking.

## Repository Link

This project leverages the code and model from the following GitHub repository:
[TrackNetV3](https://github.com/alenzenx/TrackNetV3.git)

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)


## Introduction

This project aims to track the soccer ball during a match using deep learning techniques. The TrackNet2 model is employed to detect and track the ball in each frame of the video. The dataset used for training and evaluation is sourced from [SoccerNet](https://www.soccer-net.org/data#h.qhlkhzlxi2ya).

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/Rohitkushwaha79/Soccer-Ball-Tracker.git
    cd TrackNet-SoccerBall
    ```

2. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

## Usage
### Data Download
- Download the dataset from [link](https://www.soccer-net.org/data#h.qhlkhzlxi2ya).
 
### Create Custom Soccer ball tracking Dataset
- Generate the custom dataset using the notebook [Ball_Tracking_Dataset_Creation.ipynb](notebooks/Ball_Tracking_Dataset_Creation.ipynb).
- Dataset File Structure:
```
  Ball_Tracking_Dataset
    ├─ train
    |   ├── match1/
    |   │   ├── csv/
    |   │   │   └── SNMOT-116_ball.csv
    |   │   └── frame/
    |   │       └── SNMOT-116/
    |   │           ├── 1.png
    |   │           ├── 2.png
    |   │           ├── …
    |   │           └── 750.png
    |   ├── match2/
    |   │   ├── csv/
    |   │   │   └── SNMOT-117_ball.csv
    |   │   └── frame/
    |   │       └── SNMOT-117/
    |   │           ├── 1.png
    |   │           ├── 2.png
    |   │           ├── …
    |   │           └── 750.png
    |   ├── match3/
    |   │ ⋮
    |   └── match57/
    └── test
        ├── match1/
        │   ├── csv/
        │   │   └── SNMOT-116_ball.csv
        │   └── frame/
        │       └── SNMOT-116/
        │           ├── 1.png
        │           ├── 2.png
        │           ├── …
        │           └── 750.png
        ├── match2/
        │ ⋮
        └── match49/

```
### Training

```bash
python train.py --num_frame 3 --epochs 30 --batch_size 4 --learning_rate 0.001 --save_dir exp
```
### Forecast

```bash
python predict.py --video_file=test.mp4 --model_file=exp/model_best.pt --save_dir pred_result
```

## Results
After training  model, got 63% test accuracy.

![performance](https://github.com/Rohitkushwaha79/Soccer-Ball-Tracker/assets/118690283/56bece4d-5ca2-4990-b591-5084ce64f2de)

### Prediction on video


https://github.com/Rohitkushwaha79/Soccer-Ball-Tracker/assets/118690283/f589b15e-96a5-46f1-b807-620172e1c3b6




