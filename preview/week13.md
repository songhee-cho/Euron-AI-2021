### **1. Lecture's Agenda 🍐**

- **Reinforce Learning**

### **2. Several Note-takings about the Lecture(내용 정리) 🧙**

- **Policy Gradient**
   앞에서 policy parameterization 방법을 위한 performance를 정의하면서 true value function v_{\pi_{\boldsymbol{\theta}}}이 사용되었다. 문제는 performance가 action과 states 모두의 함수라는 점이며, 이 둘은 policy weight의 영향을 받는다. state가 주어지면, policy parameterization정보로 부터 action(결국, reward)에 미치는 policy weights의 영향을 비교적 명확하게 계산될 수 있다. 그러나, policy가 state distribution에 미치는 영향은 온전히 environment의 함수이며, 알 수 없는 것이다. 그렇다면, 우리는 어떻게 policy가 영향받는 state distribution을 모른 상태에서 이 모르는 정보에 영향받는 policy weights의 performance gradient를 추정할 수 있을까? (글이 너무 복잡하다. 요점은 performance는 policy weights에 영향을 받는 state와 action의 함수이지만, 알 수 없는 state에 대한 정보가 없으면 gradient를 구할 수 없다는 얘기다.)
   
### **3. Summary(알게 된 내용 요약) 🧠**
- Policy Gradient
- Reinforce Algorithm

