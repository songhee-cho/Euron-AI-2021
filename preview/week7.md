### **0. Before the Class**

  
### **1. Lecture's Agenda 🍐**

- **Fancier Optimization**
- **Regularization**
- **Transfer Learning**

### **2. Several Note-takings about the Lecture(내용 정리) 🧙**

- **Fancier Optimization:** 
  - problems with SGD
    - loss function has high condition number
    - local minima
    - saddle point: common in high dimension
    - gradients com from minibatches: noisy
  - SGD + momentum term
  ```python
  vx = 0
  while True:
    dx = compute_gradient(x)
    vx = rho * vx + dx // vx: velocity, rho: friction coefficient
    x += learning_rate * vx
  ```
  - Nesterov momentum
    - functioning well in convex optimization
    - functioning badly in nonconvex optimization like NN
  - Adagrad
    - grad squared term 
     ```python
    grad_squared = 0
    while True:
      dx = compute_gradient(x)
      grad_squared += dx * dx
      x -= learning_rate * dx / (np.sqrt(grad_squared) + 1e-7)
    ```
  - RMSProp
  - Adam(almost)
  - Adam(full form)
  
- **Regularization**
  - L1 regularization, L2 regularization 
  - dropout
  - data augmentation
  - batch normalization also can bring regularization effect
  
- **Transfer Learning**
  - have some dataset of interest but it has <~1M images
  - can use pretrainined with similar data 


### **3. Summary(알게 된 내용 요약) 🧠**
- optimization
  - momentum, RMSProp, Adam 
- regularization
  - dropout 
- transfer learning   
