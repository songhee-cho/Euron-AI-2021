### **0. Before the Class**

- we define
    - score function: s = f(x;W) = Wx
    - SVM loss: L_i = Σ j≠y_i max(0, s_j - s_y_i + 1)
    - data loss + regularization:  L = 1/N Σ i=1~N (L_i) + Σk ((W_k)^2)

    → still want to minimize loss function : gradient of L with respect to W = ∇wL → optimization

    - optimization
        - gradient descent: numerical gradient, analytic gradient

### **1. Lecture's Agenda 🍐**

- **Backpropagation**
- **Gradients for vectorized code**
- **Neural Network**
- **Neuron and Neural Network**

### **2. Several Note-takings about the Lecture(내용 정리) 🧙**

- **Backpropagation:** computation graph ← chain rule
    - we want: ∂f/∂x, ∂f/∂y, ∂f/∂xz
        - ∂f/∂x = ∂f/∂q * ∂q/∂x
        - local gradient: ∂z/∂x, ∂z/∂y
        - gradient: ∂L/∂z
        - gradient = local gradient × upstream gradient

- **Gradients for vectorized code:** Jacobian matrix ∂f/∂x
  - Jacobian matrix: expression of derivatives in multivariable function
  - size of Jacobian matrix = (input size)×(input size)
  - size of gradient = size of variable : they should have the same shape with each other

- **Neural Network**
  - linear score function: f = Wx 
  - 2-layer neural network: f = W2(max(0,W1x))
  - 3-layer neural network: f = W3(max(0,W2(max(0,W1x))))

- **Neuron and Neural Network**
  - axon form a neuron: x0
  - synapse: × w0
  - dendrite: w0x0
  - cell body: Σ wixi + b
  - activation function: f
  - output axon: f(Σ wixi + b)
  - but acutally, biological neuron and nerual network are different 
  
### **3. Summary(알게 된 내용 요약) 🧠**
- backprop uses chain rule
- brain ananlogy of neural network is just conceptual one, and neural net is actually different from biological brain network.
