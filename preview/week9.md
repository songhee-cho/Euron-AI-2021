### **0. Before the Class**

### **1. Lecture's Agenda 🍐**: CNN Architectures

- **Case Studies**
  - AlexNet
  - VGG
  - GoogLeNet
  - ResNet
  - NiN(network in network)
  - Wide ResNet
  - ResNeXT
  - Stochastic Depth
  - DenseNet
  - FractalNet
  - SqueezeNet   

### **2. Several Note-takings about the Lecture(내용 정리) 🧙**

- **AlexNet** 
  - Conv layer → Max pooling → normalization
  - CONV1 → MAX POOL1 → NORM1 → CONV2 → MAX POOL2 → NORM2 → CONV3 → CONV4 → CONV5 → MAX POOL3 → FC6 → FC7 → FC8
  - output size = (input size - filterSize)/stride + 1
  - what is the # of parameters in max pooling layer?: # of parameters = 0
  - details of *AlexNet*
    - first use of ReLU
    - used Norm layers(not common anymore)
    - heavy data augmentation
    - dropout 0.5
    - batch size 128
    - SGD momentum 0.9
    - learning rate 1e-2, reduced by 10 manually when val accuracy plateaus
    - L2 weight decay 5e-4
    - 7 CNN ensemble

- **VGGNet**
  - small filters, deeper networks
  - why use smaller filters? (3×3 conv)
    - stack of three 3×3 conv(stride 1) layers has same effective receptive field as one 7×7 conv layer
  - most memory is in early CONV
  - most params are in late FC

- **GoogLeNet**
  - 22 layers
  - efficient "inception" module
    - inception module: design a good local network topology(net within net) and then stack these modules on top of each other
  - No FC layers
  - Only 5 million params: 12x less than AlexNet 
    
### **3. Summary(알게 된 내용 요약) 🧠**
  - AlexNet
  - VGG
  - GoogLeNet
  - ResNet
  - NiN(network in network)
  - Wide ResNet
  - ResNeXT
  - Stochastic Depth
  - DenseNet
  - FractalNet
  - SqueezeNet   
