# Lecture2: Image Classification pipeline

### **0. Before the Class**
- Numpy: efficient vectorize operation

### **1. Lecture's Agenda 🍐**
- **Introduction to Image Classification methods**
  - **K-Nearest Neighbor(K-NN)**
  - **Linear classifiers: SVM, Softmax**
  - **Two-layer neural network**
  - **Image features**

### **2. Several Note-takings about the Lecture(내용 정리) 🧙**

- **Image Classification**
    - a core task in computer vision
    - **Problem**: semantic gap
      - there is a gap btw semantic idea and pixel values of an image.
     
    - **Challenges**
      - 1. viewpoint variation
      - 2. illumination
      - 3. deformation
      - 4. occlusion
      - 5. background clutter
      - 6. intraclass variation
      
    - **Structure of image classifier**
      - there is no obvious way.
      - there is an attemp to extract features of images with finding edges, corners and boundaries.
    
    - **Data-driven approach**
      1. Collect a dataset of images and labels
      2. Use ML to train a classifier
      - there are basically two functions in a classifer: **train function** and **predict function**
      3. Evaluate the classifier on new images
      
    - 1st classifier: **Nearest Neighbor**
      - **distance metric** to compare images: **L1 distance**
      - memorize training data
      - for each test image, find closest train image and predict label of **nearest image**
      - with N examples, how fst are training and prediction?: Train O(1), Predict O(N)
      
        : classifiers should be **fast** at prediction; **slow** for training is ok
        
        : when a model is deployed, it should be fast, however, nearest-neighbor is slow at prediction.
       
     - 2nd classifier: **K-Nearest Neighbors**
        - instead of copying label from nearest neighbor, take majority vote from K closet points
        - **distance metric**: L1, L2
        - 1. **L1**: Manhattan distance; more dependent on corrdinate system
        - 2. **L2**: Euclidean distance
        - different distance ⇒ different assumption
        - **never used on image**
        - 1. very slow at test time
        - 2. distance metrics on pixel are not informative(not very good measure for img classification
        - ex. {original, boxed, shifted, tinted} imgs usually have the same L2 distances
        - 3. curse of dimensionality

    - **Hyperparameters**
      - **choices about the algorithm that we set** rather than learn
      - such as k and distance metric in K-NN
      - these are very **problem-dependent**: must try them all out and see what works best
      - when setting hyperparameters
      - 1. split data into **three groups**(**train, val, and test**); choose hyperparameters on val and evaluate on test
      - 2. **cross-validaiton**: split data into **folds**: useful for small datasets, but not used too frequently in DL
      - choose hyperparmeters using the **validation set**, **NOT test set**

- **Linear Classification**: superimportant
  - linear classifers ⇒ neural network
  - linear classifer: f(x,W) = Wx + b
    - **x**: input image
    - **W**: parameters ir weights
    - **b**: bias(considering unbalance of dataset)
    - **f(x,W)**: score function of classifier
    

- **Coming up!**
  - **Loss function**: quantifying what it means to have a "good" W
  - **Optimization**: start with random W and find a W that minimizes the loss
  - **ConvNets**: tweak the functional form of f

### **3. Summary(알게 된 내용 요약) 🧠**

- K-NN methods are not very good for image classification.
- It's important to try classification models all out for choosing the best hyperparameters.

### **4. 질문 🤔**

