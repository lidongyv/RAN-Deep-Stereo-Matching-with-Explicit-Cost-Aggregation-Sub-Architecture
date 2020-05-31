# Deep Stereo Matching with Explicit Cost Aggregation Sub-Architecture
This is the realization of the AAAI18 paper "Deep Stereo Matching with Explicit Cost Aggregation Sub-Architecture".
The project is realized by Tensorflow 0.12.
This project is built based on GCNet which u can refer to https://github.com/lidongyv/GCNet.
The key code is in the model.py which are the refer, simulate and aggregate function.

And there are some instructions about our work:

1.This AAAI work is trained and tested under four times sub-sampling, which means on SceneFlow the image size is 135x240 so does it on KITTI. The sub-sampling operation is indispensable, because the global view plays a crucial part to obtain the structure information for the guidance branch, while the volume style in the network will take a lot of storage. But you can modify the size if your GPU is powerful enough.

2. If you does the experiments not only on SceneFLow and KITTI, the fusion function can be modified to reach a better results, you can refer to the paper of two-stream network proposed by Pro. Zisserman of Oxford.

3. There are a few advices for you if you want to take fully advantages of our work. You can reproduce a more efficient baseline, since the GC-Net did not publish their code, the GC-Net I reproduce did not reach the extract same error rate of the GC-Net of Alex Kendall. We also do some experiments with other baselines, the promotion of our cost aggregation method still remains. 
