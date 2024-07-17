## 밑작업 및 오류 정리

---

해당 문서는 공부 도중 겪은 오류 혹은 필요하다고 생각한 조치 사항 등을 정리해놓은 글입니다.

### 0. Pycharm에서 Anaconda 가상 환경 사용하기

---

1. **Anaconda 설치**  

[설치 url(https://www.anaconda.com/download)](https://www.anaconda.com/download)

2. **prompt에서 Anaconda 가상 환경 생성**

Anaconda Prompt 창에서 가상환경 생성
~~~
conda create -n (name) python=(version)
~~~
3. **Pycharm에서 가상환경 연결**

File - Settings - Project - Python Interpreter 에서 생성한 anaconda 가상 환경으로 변경

<img src="https://github.com/user-attachments/assets/ee61bf62-5a1d-431a-92ce-75bee0b8d55a" height="250">
<img src="https://github.com/user-attachments/assets/28ba7034-c380-4f2e-ba42-4abe9a540e72" height="350">

conda 가상 환경이 없을 경우, Add Interpreter - Conda Environment 에서 찾아서 추가

<img src="https://github.com/user-attachments/assets/e8556685-01e3-4710-acbd-7ae9d222e064" height="250">

### 1. GPU로 Keras 학습하기

---

GAN 모델부터 CPU로 학습하면 너무 느리기에 앞으로도 결국 GPU를 사용해야 할 것 같아 GPU로 학습하는 방법을 찾아봤다.

window에서 GPU를 지원하는 tensorflow는 2.1.0 버젼까지만 존재하고 
해당 버젼은 cuDNN은 8.1, CUDA 11.2와 호환되는데 CUDA 11.2는 window 11 설치 파일이 존재하지 않는다.

가상 환경에서 CUDA, cuDNN 버젼을 제한하는 방법도 있는 것으로 보이지만 향후를 위해 WSL을 사용하는 것이 나아보여 해당 방법을 찾아보았다.
