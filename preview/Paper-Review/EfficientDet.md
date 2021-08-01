## Topic: ```Object Detection```
### EfficientDet
- **Name of Thesis:** EfficientDet: Scalable and Efficient Object Detection
- **Link:** https://arxiv.org/abs/1911.09070

### **Abstract**🍐
Model efficiency has become increasingly important in computer vision. 
In this paper, we systemically study neural network architeture design choices for ```object detection``` and propose several key optimizations to imporve efficiency.
First, we propose ```a weighted bi-directional feature pytramid network(BiFPN)```, 
which allows ```easy and fast multi-scale feature fusion;
Second, we propose a compound scaling method``` that uniformly scales the resolution, depth, and width for all backbone,
feature network, and box/class prediction networks at the same time.
Based on these optimizations and better backbones, we have developed a new familiy of object ddetectors,
called *EfficientDet*, which consistently achieve much better efficienvy than prior art 
across a wide spectrum of resource constraints.
In paricular, with single-model and single-scale, 
***
our **EfficientDet-D7** achcieves
**SOTA 55.1AP on COCO test-dev with 77M parameters and 410B FLOPs**, 
**being 4x-9x smaller and using 13x-42x fewer FLOPs** than previous detectors. 
***



