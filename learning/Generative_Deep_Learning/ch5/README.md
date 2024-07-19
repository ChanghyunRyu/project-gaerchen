## Chapter 5. 자기회귀 모델(Autoregressive Model)

---

**LSTM(Long Short-Term Memory network)는** 순환 신경망(RNN, Recurrent Neural Nework)의 한 종류입니다.
기존 RNN의 문제인 기울기 소멸 문제를 방지하도록 개발되었다. 

RNN은 입력과 출력을 시쿼스 단위로 처리하는 시퀀스 모델입니다. 인간은 생각을 처음부터 시작하지 않습니다.
무언가 글을 읽거나 생각을 할 때도 지금까지의 경험을 토대로 이를 해석합니다. 일반적인 nerual network는 이처럼 동작하지 않습니다.

Recurrent neural network(RNN)은 이러한 일반적인 nerual network의 문제점을 해결하고자 만든 모델입니다.
RNN은 아래 그림처럼 유닛 간의 연결이 순환적 구조를 가지는 특징이 있습니다. 

<img src="https://github.com/user-attachments/assets/dd37c716-369a-4a48-af6f-844a424de460">

RNN이 처음 소개되었을 때, 층 구조가 단순했고 tanh 함수 하나로 구성되었습니다.
그러나 이러한 방식은 **기울기 소멸 문제(Gradient vanishing)가** 나타나 시퀀스가 너무 긴 데이터에서는 사용하기 힘듭니다.

