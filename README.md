# DL-hw1-taskA
This project implements a special convolution module called `DynamicChannelConv`, designed to handle arbitrary input channel combinations (e.g., RGB, RG, R, G, B). It enables CNNs to dynamically adapt to different input formats without retraining.

## How to Run
1. Change the `image_dir` variable in the code to the path of your local image folder.

## Features
This script will:
1. **Train 4 configurations of `DynamicChannelConv`**:
   - `(hidden_dim=64, out_channels=64)`
   - `(hidden_dim=128, out_channels=64)`
   - `(hidden_dim=128, out_channels=32)`
   - `(hidden_dim=128, out_channels=128)`
2. **Test across 7 channel combinations**:
   - `RGB`, `RG`, `RB`, `GB`, `R`, `G`, `B`
3. **Train a baseline fixed-channel CNN model (RGB only)**
4. **Generate and plot**:
   - Accuracy on test sets for each configuration
   - FLOPs and parameter counts (`thop`-based)
   - Line plots of accuracy, FLOPs, and Params

## Output
- Printed metrics: Accuracy, FLOPs (in Millions), Params (in Thousands)
- 3 plots showing performance comparisons by channel/model configuration

## Notes
- All training runs use **3 epochs** for rapid benchmarking
- Batch size = 32, optimizer = Adam, learning rate = `1e-3`
- FLOPs and parameter counts are computed using the `thop` package
- Suitable for quick analysis, ablation testing, and hardware-aware design

