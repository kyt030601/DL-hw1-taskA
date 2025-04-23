# DL-hw1-taskA
This project implements a special convolution module (`DynamicChannelConv`) that supports **arbitrary input channel combinations** (such as RGB, RG, R, G, B). It includes full training, testing, ablation experiments, and FLOPs/parameter analysis.

Q:How to run?    
A:Change the image_dir in the program to the path of your own folder and you can use it

This will:    
1.Train 4 different DynamicConv configurations:    
  -(hidden_dim=64, out_channels=64)    
  -(hidden_dim=128, out_channels=64)    
  -(hidden_dim=128, out_channels=32)    
  -(hidden_dim=128, out_channels=128)    
2.Test each configuration on 5 channel combinations: RGB, RG, R, G, B    
3.Train a baseline CNN model (fixed RGB input)    
4.Report:    
  -Accuracy for all models and all channels    
  -Training loss per epoch    
  -FLOPs and parameter count for each model    

Note:    
1.All training runs are only 3 epochs for quick comparison.    
2.FLOPs/Params are calculated using thop.    
