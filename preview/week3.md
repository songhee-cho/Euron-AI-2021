# Lecture3: Loss function and Optimization

### **0. Before the Class**

- **Recall from last time**
    - Challenges of recognition: viewpoint, illumination, deformation, occlusion, clutter, intraclass variation
    - data-drive approach: kNN
    - linear classifier: parametric model → loss function & optimization

### **1. Lecture's Agenda 🍐**

- **Introduction to Image Classification methods**
    - **K-Nearest Neighbor(K-NN)**
    - ***Linear classifiers: SVM, Softmax***
    - **Two-layer neural network**
    - **Image features**

### **2. Several Note-takings about the Lecture(내용 정리) 🧙**

- **Loss function**: quantifying what it means to have a "good" W

    - **use "-log" instead of "log**: actually loss function quantifying badness of model, so in order to make the output of loss function become 1 when   
    - **Multiclass SVM Loss (=Hinge Loss)**: Multiclass Support Vector Machine loss
        - Δ(margin): hyper-parameter
        - using Max

    - **Softmax Classifier:** multinomial logistic regression
      - logistic regression: sigmoid
      - calculate probability using exp
      - sentive to data

    - **Data loss** and **Regularization loss**
        - **Regularization**: L1 normalization, L2 normalization
        - λ: hyper-parameter, control the normalization; if λ increases, the model becomes simple since regularization loss increases 

- **Optimization**: start with random W and find a W that minimizes the loss
  - **slope → gradient(vector)** 
  - **numerical gradient**
  - **3 step to caculate numerical gradient**
    - (1) W
    - (2) increment 1st element of W by a small value h
    - (3) recompute the loss

  - **analytic gradient**
  - **gradient check**
  - **gradient descent(GD)**
  - **stochastic gradient descent(SGD)**: random mini batch
  - **RMSprop**: step size
  - **Adam**: momentum
  
- **Image Features**: color histogram(color spectrum), HoG(edge orientation), bag of words(benchmarked from NLP)
- **ConvNets**: tweak the functional form of f
 

### **3. Summary(알게 된 내용 요약) 🧠**

- We should decide normalization method according to how the complexity of a data needs to be reflected to a model.
- Differences between various optimizers(SGD, RMSprop, Adam)
