### **0. Before the Class**

- History of CNN
  - 1957, perceptron: weight W update rule → w<sub>i</sub>(t+1) = w<sub>i</sub>(t) + α(d<sub>j</sub> - y<sub>j</sub>(t))x<sub>j,i
  - 1960, multilayer perceptron network
  - 1986, backpropagation: ∂E<sub>p</sub>/∂w<sub>ji</sub> = ∂E<sub>p</sub>/∂o<sub>pj</sub> * ∂o<sub>pj</sub>/∂w<sub>ji</sub>
  - 2006, deep learning
  - 2012, AlexNet → CNN, batch normalization
  
### **1. Lecture's Agenda 🍐**

- **Architecture of CNN**
- **Layers of CNN**
- **Structure of CNN**

### **2. Several Note-takings about the Lecture(내용 정리) 🧙**

- **Architecture of CNN:** computation graph ← chain rule
    - fully connected layer(FC layer/Dense Layer/Flatten Layer): 32×32×3 → 3072×1(input) ⇒ Wx ⇒ activation layer: 1×10
    - convolutional layer: 32×32×3(input)⇒ 5×5×3 filter: spatially dot product
      - filter slides over the input image(convolve) several times: w<sup>T</sup>x + b
      - activation map
      - the number of filters, the size of filters, stride
    
- **Layers of CNN:** 
  - convolutional layer
    - local connectivity
    - spatial arrangement
    - parameter sharing
  - pooling layer: commonly use maxpooling
    - to reduce the number of parameters(computation)
  - fully-connected layer
  
- **Structure of CNN**
  - INPUT ->  ((CONV -> RELU) x N -> POOL?)x M -> (FC -> RELU) x K -> FC
    - POOL?: optional
    - K activations
    - commonly 0<=N<3, M>=0, 0<=K<3

### **3. Summary(알게 된 내용 요약) 🧠**
- ConvNets stack CONV, POOL, FC layers
- Trend: smaller filers, deeper architectures, getting rid of POOL/FC
- ResNet, GoogLeNet
