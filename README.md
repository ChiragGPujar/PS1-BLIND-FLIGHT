# PS1-BLIND-FLIGHT
This repository contains the full pipeline for solving PS1 Blind Flight challenge using:
  Convolutional Neural Network for tile classification
  Boost-aware cost model
  A* shortest path planning
  Robust fallback & error-safe engineering

Instructions to Reproduce Results: 
1) Since the dataset is ~17GB, use Kaggle Notebook:
    Go to competition page
    Click Code → New Notebook
    Attach competition dataset under Add Input → Competition Data

2) Install/Patch Dependencies if required:
   pip install protobuf==3.20.3
   pip install tensorflow==2.12.0

3) Run Training:
   Execute training notebook/script:
     Extracts tiles
     Trains CNN tile classifier
     Saves model as: /kaggle/working/tile_cnn.h5

4) Run
   Execute inference notebook/script:
   This performs:
     CNN-based tile perception (batched, fast)
     Terrain detection
     Cost-aware A* path planning
     Robust fallback system to avoid crashes
     Creates submission file
%) Submit the file to Kaggle.
