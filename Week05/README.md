# Data Visualization

#### Polar Plot
*  극 좌표계를 사용하는 시각화
*  회전이나 주기성을 표현하기 좋다
![image](https://user-images.githubusercontent.com/44192730/153590785-d23f2f68-176e-4d74-ba58-7eb1101870ee.png)

#### Radar Plot
* feature가 많아지거나 순서가 바뀌면 인지하기 힘들다는 단점이 있다
![image](https://user-images.githubusercontent.com/44192730/153590959-94de714e-b652-4e84-8622-ddb560c97ebd.png)

#### Pie Chart
* 전체를 백분위로 나타낼 때 유용
* 많이 사용되지만 지양할 필요가 있다 (참고 자료 확인)

#### ETC
* Missingno : 결측치 시각화
* Treemap : 계층적 데이터를 시각화 할 때 유용
* Waffle Chart
* Venn : 집합을 표현할때 사용 (벤 다이어그램)

---
# DL Basic
### MLP
* Data, Model, loss 로 크게 구분
* 연산이 진행되면서 loss를 줄이는 방향으로 update

#### Optimization
* Generalization : Test error 와 train error 사이의 gap이 얼마나 적냐에 따라 generalization을 확인할 수 있다.
* Cross-validation : input data에 독립적인(generalize) 모델을 학습하기 위해 사용하는 기법

* Gradient Descent Methods
  * SGD : 확률적 경사 하강법
  * Momentum : 학습의 가속도를 정해주는 기법
  * Nesterov Accelerated Gradient : 모멘텀 방향으로 먼저 점프를 하고, 이 방향을 기울기 업데이트와 함께 수정
  * Adagrad : 학습률이 너무 작으면 학습 시간이 너무 길고, 너무 크면 발산해서 학습이 제대로 안되기 때문에 학습률 감소(learning rate decay)를 적용
  * RMSprop : Adagrad에서 minima에 도달하지 않았음에도 학습률이 0이 될 수 있기에, 최신 기울기가 더 반영되도록 적용
  * Adam : Momentum 과 AdaGrad를 적용한 방법

* Regularization
  * Early stopping : 적정한 선에서 학습을 종료해준다
  * parameter norm penalty : cost를 smoothing 해준다
  * data augmentation : DL에서는 많은 데이터를 확보하면 좋기 때문에 사용한다
  * noise robustness : random noise를 추가해 준다 (이미지)
  * label smoothing : training 데이터를 적절히 mix하여 학습에 사용
  * dropout : forward pass시 random 하게 neurons를 0으로 만들어준다 
  * batch normalization : 각 차원에 대해 mean, variance를 이용해 normalize해준다

### CNN
* Stride : filter를 몇칸씩 이동할지
* padding : filter 사용시 이미지 외곽을 어떤 데이터로 추가해 줄지
* 1x1 Convolution : MLP를 사용하지 않고 dimention reduction을 위해 사용해준다 (파라미터가 많이 감소)

### CNN Models
* Alexnet : 여러개의 convolution net을 중첩, 마지막은 dense layer를 사용한다,Rulu function, Data augmentation, dropout을 사용
* VGGNet : layer를 많이 쌓을 수록 더 좋은 성능을 기대
* GooLeNet : inception block (1*1 conv)를 사용하여 파라미터 수를 낮춰주었다
* ResNet : 너무 많은 param에 의해 overfitting이 되는 것을 막기 위해 skip connection을 사용 (성능은 늘고, 파라미터는 감소)
* DenseNet : addition 대신 concatenation을 사용

# Vision
* Segmantic Segmentation : 픽셀 단위의 분류, deconvolution이 사용
![image](https://user-images.githubusercontent.com/44192730/153594917-a7360e0b-5454-4ad6-b379-fb5e53fd57b9.png)

* Detection
  * R-CNN : region별 분류를 통해 탐지
  * SPPNet
  * Fast R-CNN : class와 bounding-box regressor를 동시에 수행
  * Faster R-CNN
  * YOLO : grid를 통해 bounding-box regressor 분류를 한번만 실행

---
# RNN
* 순서가 있는 데이터를 위한 모델
* input - hidden state - Output 형태
![image](https://user-images.githubusercontent.com/44192730/153595537-21de722d-53ef-4a36-a50c-26b5e288c4b2.png)

* LSTM : rnn의 gradient vanishing/exploding 문제를 해결하기 위해 제안 
![image](https://user-images.githubusercontent.com/44192730/153595601-6496367d-0eb7-48df-81c3-b5dac2531cbf.png)

* GRU
---
### Transformer
* attension을 사용한 모델
* RNN처럼 순차적을 학습을 하지 않아도 된다
* ViT 처럼 vision 문제에서도 많이 쓰인다

### GAN
* Generator와 discriminator간 학습을 통해서 진짜같은 가짜를 생성해내는 모델

---

* 참고자료
* AI boostcamp 강의를 참고하여 정리한 자료입니다.
* https://m.blog.naver.com/sw4r/221231919777
* https://light-tree.tistory.com/140
#### Pie Chart 참고
* https://www.readcube.com/articles/10.3138%2Fjsp.46.3.05
* https://funnel.io/blog/why-we-dont-use-pie-charts-and-some-tips-on-better-data-visualizations
