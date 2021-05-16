### **0. Before the Class**

- computational graphs: f = Wx + regularization
- neural net: hidden layers
- CNN: separate activation maps
- mini-batch SGD

  
### **1. Lecture's Agenda 🍐**: training neural nets

- **Activation Functions**
- **Data Preprocessing**
- **Weight Initialization**
- **Batch Normalization**
- **Babysitting the Learning Process**
- **Hyperparameter Optimization**

### **2. Several Note-takings about the Lecture(내용 정리) 🧙**

- **Activation Functions:** 
   - sigmoid function
      - gradient vaninshing satured neurons kill the gradients → problematic during backpropagation
      - outputs are not zero-centered
      - exp() is a bit compute expensive
  - tanh
  - ReLU
    - people like to initialize ReLU neurons with slightly positive biases
  - Leaky ReLU & PReLU
  - ELU
  - Maxout
    
- **Data Preprocessing**
  - zero-centered & normalized data
    - np.mean, np.std
  - PCA & whitening
    - PCA: decorrelated data, data has diagonal covariance matrix
    - whitened data: covariance matrix is the identity matrix
   - image data preprocessing
      - commonly preprocess until zero-centered
  
  
- **Weight Initialization**
  - small random numbers
  - large random numbers
  - Xavier initialization

- **Batch Normalization**
  - prevent gradient vanshing
  - prevent covarience shift
  - do not have to be used when dropout is applied
  
- **Babysitting the Learning Process**
  - 1) preprocess the data
  - 2) chose the architecture
  - 3) double check that the loss is reasonable

- **Hyperparameter Optimization**
  - cross-validation strategy
    - random search vs grid search
  - network architeture, learning rate, its decay schedule, update type, regularization

### **3. Summary(알게 된 내용 요약) 🧠**
- **Activation Functions**: use ReLU
- **Data Preprocessing**: images; subtract mean
- **Weight Initialization**: use Xavier init
- **Batch Normalization**: use
- **Babysitting the Learning Process**
- **Hyperparameter Optimization**: random samples
