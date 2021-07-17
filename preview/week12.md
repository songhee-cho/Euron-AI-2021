### **1. Lecture's Agenda 🍐**

- **Generative Models**

### **2. Several Note-takings about the Lecture(내용 정리) 🧙**

- **Supervised vs Unsupervised Learning**
    - Unsupervised Learning
      - Just data, no labels
      - *Goal*: Learn some underlying, hidden structure of the data
      - Exp: Clustering, Dimensionality reduction, Autoencoders(feature learning), Density estimation, etc  
    
    - Generative Models
      - Given training data, generate new samples from same distribution
      - Explicit density
      - Implicit density

  - PixelRNN
    - Generate image pixels starting from corner
    - Dependency on previous pixels modeled using an RNN(LSTM)
    - *Drawback*: sequential generation is slow

  - PixelCNN
    - Still generate image pixels starting from corner
    - Dependency on previous pixels now modeled using a CNN over context region
    - *Training*: maximize likelihood of training images


  - Autoencoders
    - Encoder can be used to initialize a supervised model
    - VAE(Variational Autoencoders): Intractability; define intractable density function with latent z
                                     cannot optimize directly, derive and optimize lower bound on likelihood instead
                                     
  - Training GANs
    - Generator network: gradient ascent 
    - Distriminator network 
  
### **3. Summary(알게 된 내용 요약) 🧠**
- Generative Models
  - PixelRNN and PixelCNN
  - VAE
  - GANs 
