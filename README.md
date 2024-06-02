# TrackNet-SoccerBall

TrackNet-SoccerBall is a project for tracking the soccer ball in a soccer match using the TrackNet model. This project leverages the TrackNetV3 model to accomplish accurate and efficient ball tracking.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [Credits](#credits)
- [License](#license)

## Introduction

This project aims to track the soccer ball during a match using deep learning techniques. The TrackNetV3 model is employed to detect and track the ball in each frame of the video. The dataset used for training and evaluation is sourced from [SoccerNet](https://www.soccer-net.org/data#h.qhlkhzlxi2ya).

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/TrackNet-SoccerBall.git
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
- Generate the custom dataset using the notebook [SoccerNet_Jersey_Extraction_Dataset_Creation.ipynb](notebooks/SoccerNet_Jersey_Extraction_Dataset_Creation.ipynb).
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

## Credits

This project is based on the [TrackNetV3](https://github.com/alenzenx/TrackNetV3.git) repository. Full credit goes to the original authors for their work on the model.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
