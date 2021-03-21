# preview-week1.md

### **1. Lecture's Agenda 🍐**

* **A brief history of computer vision**

* **CS231n overview**

### **2. Several Note-takings about the Lecture(내용 정리) 🧙**

* **A brief history of computer vision**
  -  **Block world(Larry Roberts, 1963)**: early 1960' was the start of computer vision.
  -  **The summer vision project of MIT(Saymour Papert, 1966)**: it's an attempt to construct a significant part of a visual system(pattern recognition).
  -  **VISON(David Marr, 1970')**: input image → primal sketch →  2.5D sketch →  3D model
  -  **Similar ideas in 1970'**: (every obj → simple geometric primitives), (complex structure → collection of simpler shapes & geometric configuration)
      -  Generalized cylinder(Brooks & Binford, 1979)
      -  Pictorial structure(Fischelr and Elschlager, 1973)
  - **Face detection(Viola & Johnes, 2001)**: real-time face detector
  - **Histogram of gradients(Dala & Triggs, 2005)**
  - **PASCAL Visual Object Challenge(2006~2012)**: 20 obj categories
  - **ImageNet**: solve a harder question, to recognize every objects.
    - most of ML algorithms such as graphical machine, SVM, AdaBoost was very easy to overfit due to the complexity of visual data.
    - an attempt to overcome dual reasons.
    - 1. images are too complex, so models have to have high dimension of input and a lot of parameters to fit.
    - 2. if training data is not enough , overfitting happens so fast.
    - Error rate of models using ImageNet is steadily decreasing. Especially, 2012 was the breakthrough moment.

* **CS231n overview**
  - CS231n focuses on one of the most important problems of visual recognition - image classification.
  - There is a number of visual recognition problems that are related to image classification, such as obj detection, img captioning.
  - CNN(Convoutional Neural Networks) have become an important tool for obj recognition.
    - large scale visual recognition challenge: deeper networks / NEC-UIUC → SuperVision → GoogLeNet, VGG → MSRA
  - CNNs were not invented overnight.
    - CNN for recognizing digits(LeCun, 1998): transistors 
    - AlexNet(Krizhevsky, 2012): transistors, GPUs / increased computer availability, labeled datasets was comparatively enough 
  - The quest for visual intelligence goes far beyond obj recognition.
    - computer vision models that see(understand) a scene like human visual system.
    - it's far to develop network models to understand complex images. 

### **3. Summary(알게 된 내용 요약) 🧠**

- HW availablity(computational ability from GPUs, etc) and labeled data in computer vision are super-important in computer vision.
- It's still hard to understand complex images using computer vision.

### **4. 질문 🤔**

- complex structre를 simple shape으로 나타내려는 노력들(generalized cylinder, pictorial structure 등)은 연산량을 줄이기 위해서 연구된 내용인지 혹은 computer vision에서 물체를 기계가 이해할 수 있도록 만들기 위한 일종의 전처리를 시도한 것인지, 그 목적이 궁금합니다.
