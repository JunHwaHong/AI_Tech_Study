# Data Visualization

## Intro
#### 데이터 시각화란
* 데이터 시각화는 데이터 분석 결과를 쉽게 이해할 수 있도록 도표라는 시각적 수단을 통해 정보를 효과적으로 전달하는 것을 말한다

#### 데이터
* 데이터의 종류 : 정형, 시계열, 지리, 네트워크, 비정형 데이터 등

#### 시각화
* Mark : 점, 선, 면 
* Channel : 각 마크를 변경하는 요소 (position, shape, color 등)

#### 전주의적 속성 (Preattentive attribute)
* 어떤 것을 보자마자 뇌에서 바로 알아차릴 수 있도록, 강조하기 위한 시각화 속성
* 길이, 색, 속성 등
* 여러가지 혼용을 하면 인지하기 힘든 단점이 있다

#### Bar Chart
* 범주형 데이터를 비교하기 적합 (개별, 그룹 비교)
* MultipleBar Plot : 한 개의 feature에 대해서만 보여준다
* Stacked Bar Plot : 맨 밑이 아닌 데이터의 분포를 파악하기 어려운 단점이 있다
* Overlapped Bar Plot : 3개 이상에서는 파악이 어렵다는 단점
* 차트를 만들 때에는 잘못 인지될 것을 막기 위해 scale, 정렬, layout, 복잡성 등을 고려해야한다

#### Line Plot
* 구성 요소 : 색상, 마커, 선 종류
* 구체적인 데이터 보다 추세 확인을 목적으로 smoothing이 필요한 경우도 있다.
* 간격을 명시해 주어 없는 데이터에 대한 오해를 줄여주는 것이 좋다

#### Scatter Plot
* 점을 사용하여 두 feature간의 관계를 확인할 때 많이 사용한다 (상관관계 확인)
* 구성 요소 : 색, 모양, 크기
* 분포를 파악하기 쉽게 여러 방법을 사용 (투명도 조절, contour plot 등)

#### Text 사용
* Title, Label, Tick Label, Legend, Annotation

#### Color
* 위치와 색은 가장 효과적인 방법
* 인지를 쉽게 할 수 있는 색 선택이 중요

#### Facet
* 화면상 view를 분할하여 여러 관점을 보여줄 수 있다
* subplot, grid spec 활용

#### ETC
* Grid, 참고 선, 면 추가, theme 바꾸기 등 


---
* 데이터 분석 결과를 시각화 하는 것에 대한 중요성을 다시 한번 생각하게 되었다.
* 데이터 시각화에 필요한 여러 요소들을 배웠다.
* AI 뿐만 아니라 어떠한 Application이라도 User가 사용하기 쉽게 만들 수 있도록 UX에 대한 고려를 많이 해야 한다는 것을 느끼게 되었다.
* 평소에도 다양한 contents를 볼때 UI/UX를 관심있게 보면 좋을 것 같다.

---

* 참고자료
* AI boostcamp 강의를 참고하여 정리한 자료입니다.
* 도서 
  * Visualization Analysis and Design Principles, Techniques, and Practice
  * Fundamentals of Data Visualization A Primer on Making Informative and Compelling Figures
* 블로그
  * https://visualize.tistory.com/112
  * https://karl6885.github.io/visualization/2019/03/13/%EB%8D%B0%EC%9D%B4%ED%84%B0-%EC%8B%9C%EA%B0%81%ED%99%94%EC%9D%98-%EA%B8%B0%EB%B3%B8/
