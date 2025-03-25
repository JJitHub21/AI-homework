인공지능 기초를 위한 FAQ

1. 인공지능에서 지능에 해당하는 기능은 무엇인가? 
=> 인공지능에서 지능에 해당하는 것은 데이터를 학습, 이해, 추론한 것을 바탕으로 문제 해결하는 기능이다.

2. 인공지능의 종류 3가지에 대해서 설명하시오 (지도학습, 반지도학습, 강화학습)
=> 지도학습: 정답이 있는 데이터를 활용하여 데이터를 학습시키는 것으로 분류, 회구로 나뉘어진다.
=> 반지도학습: 정답이 없는 데이터를 비슷한 특징끼리 군집화하여 새로운 데이터에 대한 결과를 예측하는 방법이다.
=> 강화학습: 주어지는 데이터와 정답 없이 컴퓨터가 역동적인 환경에서 반복적인 시행착오를 통해 행동에 대한 보상을 받으며 학습하여 환경 안에서 선택 가능한 행동들 중 보상을 최대화하는 행동을 찾아가는 방법이다. Alpha GO가 대표적인 강화학습의 예시이며, 지도학습으로 바둑을 학습하는 경우 너무나 방대한 경우의 수가 데이터로 주어져야하지만 딥러닝의 등장으로 신경망이 적용되면서 강화 학습으로 효과적인 바둑 학습을 할 수 있었던 것이다.

3. 전통적인 프로그래밍 방법과 인공지능 프로그램의 차이점은 무엇인가?
=> 전통적인 프로그래밍은 프로그래머가 rule을 정하고 데이터를 입력하여 정답을 출력하고, 인공지능 프로그램은 주어진 입력과 정답을 기반으로 API가 rule을 도출하여 새로운 입력에 대해 정답을 출력한다.

4. 딥러닝과 머신러닝의 차이점은 무엇인가?
=> 머신러닝은 컴퓨터가 스스로 데이터를 학습하고 예측하게 하는 것이고, 딥러닝은 머신러닝의 한 분야로서 인공신경망 등을 사용하여 빅데이터로부터 컴퓨터가 더 복잡한 학습을 할 수 있게끔 하는 기술이다.
   딥러닝은 머신러닝보다 더 많은 데이터를 바탕으로 여러 층의 신경망을 통해 복잡한 패턴을 학습하기 때문에 머신러닝보다 더 많은 데이터와 강력한 컴퓨팅 리소스를 필요로 한다.
   고로 머신러닝은 간단한 문제나 적은 양의 데이터 학습에 적합하고, 딥러닝을 복잡한 문제나 대규모 데이터 학습에 적합하다.

5. Classification과 Regression의 주된 차이점은?
=> Classification은 이산적인 값, Regression은 연속적인 값을 결과로 갖는다.

6. 머신러닝에서 차원의 저주(curse of dimensionality)란?
=> 머신러닝에서 모델이 더 많은 정보를 학습할 수 있도록 다양한 특징(feature)을 첨부하는 과정에서 차원이 증가하고, 이로 인해 학습데이터 수가 차원의 수보다 적어져 개별 차원 내 학습할 데이터의 수가 적어지면서 성능이 저하되는 현상이다.
   차원의 저주에 가장 치명적인 알고리즘으로 KNN이 있는데 KNN(K-Nearest Neighborhood, 최근접이웃) 알고리즘은 자신과 가장 가까운 이웃 K개로 결과값을 결정하는 데, 차원이 커짐에 따라 주변 이웃의 수가 점점 감소하여 정보가 적어지면서 성능 저하로 이어진다.
   차원의 저주를 해결하기 위해서는 불필요한 특성(feature)을 제거하거나 충분한 데이터를 모으는 과정을 거쳐야 한다.

7. Dimensionality Reduction는 왜 필요한가?
=> Dimensionality Reduction(차원 축소)란 고차원 데이터(many features)를 중요 특성을 유지함으로서 정보 손실 없이 더 낮은 차원(less features)으로 축소하는 기법이다.
=> (1) 차원을 축소함으로써 차원의 저주를 극복한다.
=> (2) 특성을 줄임으로써 과적합을 방지한다.
=> (3) 특성이 줄어들어 계산량이 줄고, 모델의 학습/예측 속도가 향상된다.
=> (4) 모델의 결과를 2차원이나 3차원으로 축소하여 모델이 간단해지고 내부 구조를 파악하기 쉽다.

8. Ridge와 Lasso의 공통점과 차이점? (Regularization, 규제 , Scaling)
=> 두 방법 모두 선형 회귀 모델의 과적합 방지를 위한 것으로, 정규화 기법, Scaling 작업을 통해 모델의 복잡도를 줄인다. Ridge는 L2 정규화를 통해 계수를 작게 만들고, Lasso는 L1 정규화를 통해 일부 계수를 0으로 만들어 변수 선택까지 수행한다.
/** 
Regularization: 모델이 너무 복잡하거나 과적합 되는 것을 막기 위해 손실 함수에 패널티를 추가하는 것으로 대표적인 방식은 Ridge(L2 정규화), Lasso(L1 정규화)가 있다.
Scaling: 서로 다른 단위를 가진 입력값(feature)을 비슷한 범위로 맞추는 작업이다.
L2 정규화: 모델의 가중치(m)의 제곱합을 손실 함수에 패널티로 추가하는 방식, 불필요한 특성의 값을 축소한다.
L1 정규화: 가중치의 절댓값 합을 손실 함수에 패널티로 추가하는 방식, 불필요한 특성의 값을 아예 삭제한다.
**/

9. Overfitting vs. Underfitting
=> Overfitting: 과대 적합은 학습하는 데이터에서는 성능이 뛰어나지만 새로운 데이터에 대해서는 성능이 잘 나오지 않는 모델을 생성하는 것이다. 모델이 너무 복잡하여 훈련 데이터에 섞인 노이즈까지 학습하는 등의 이유로 발생한다. 모델 단순화, 노이즈 제거, 규제 등의 방안으로 해결한다.
=> Underfitting: 모델이 너무 단순하여(혹은 데이터가 충분히 복잡하지 않은 경우) 훈련 데이터에서도 좋은 성능을 보이지 못하는 경우이다.

10. Feature Engineering과 Feature Selection의 차이점은?
=> Feature Engineering이란 머신 러닝 모델의 성능 향상을 위해 데이터의 특성(Feature)을 생성, 변환, 삭제하는 과정이다. 반면 Feature Selection은 특성을 생성하거나 변환하는 Feature Engineering과 다르게 불필요하거나 중요도가 떨어지는 특성을 제거함으로써 모델 성능을 향상 또는 단순화한다.

11. 전처리(Preprocessing)의 목적과 방법? (노이즈, 이상치, 결측치)
=> 전처리(Preprocessing)은 데이터 분석을 위해 수집한 데이터를 적절한 형태로 가공하는 과정으로서 데이터 품질 향상, 노이즈 제거, 이상치/결측치 대응을 목적으로 한다.
=> 결측치 처리: 데이터에 비어있는 값이 존재할 경우, 해당 값을 삭제하거나 평균/중앙값/최빈값 등으로 대체하여 데이터 일관성을 유지한다.
=> 이상치 처리: 평균에서 너무 떨어진 값이 존재하면 제거하거나 변환, 대체하여 처리한다.
=> 노이즈 제거: 무작위성 또는 의미 없는 값, 원본을 왜곡시키는 값의 경우 이동 평균이나 중앙값을 사용하여 스무딩(Smoothing) 처리한다.

12. EDA(Explorary Data Analysis)란? 데이터의 특성 파악(분포, 상관관계)
=> 데이터를 시각화하거나 통계적으로 분석하여, 데이터의 분포, 구조, 관계, 이상점 등을 파악하는 과정이다. EDA에서는 핵심적인 두 가지 분석인 분포와 상관관계가 있다.
=> 분포: 데이터가 주로 어떤 값들을 가지는지와 값들이 퍼져있는 형태를 확인한다. 데이터가 치우쳐 있는지, 정규분포를 따르는지, 이상치가 존재하는지 등을 확인해야 한다.
=> 상관관계: 두 변수 간에 얼마나 관련이 있는지를 나타내는 지표이다. 상관계수로 관련성을 파악하며 1에 가까울수록 양의 상관관계(비례), -1에 가까울수록 음의 상관관계(반비례), 0에 가까울수록 관련성이 적다.

13. 회귀에서 절편과 기울기가 의미하는 바는? 딥러닝과 어떻게 연관되는가?
=> 회기식 f(x) = mx + b에서 기울기(m)는 x가 1 증가할 때 f(x)가 얼마나 증감하는 지를 나타내는 값으로 특성의 중요도, 영향력을 뜻하고,
절편(b)는 모든 특성값이 0일 때 예측되는 f(x) 값이다.
딥러닝은 회귀식 f(x) = mx + b를 기본 단위로 사용하며, 각 뉴런은 기울기(w)와 절편(b)을 통해 입력값을 처리한다.
즉, 회귀는 딥러닝 구조의 핵심이자 기본 연산 블록이다.

14. 교차검증, K-fold 교차검증의 의미와 차이
=> 교차검증: 데이터를 훈련셋과 검증셋으로 여러 번 나눠가며 모델을 학습/평가하여, 과적합을 방지하고 일반화 성능을 더 정확히 측정하는 방법
=> K-fold 교차검증: 전체 데이터를 K개로 나눈 뒤, 매번 한 조각을 검증용, 나머지를 훈련용으로 사용해서 K번 학습/평가하는 방식
=> 교차검증은 모델의 일반화 성능을 평가하기 위해 데이터를 반복 분할하여 학습과 검증을 수행하는 방법이며, K-Fold 교차검증은 이를 K개로 나누어 K번 학습, 평가하는 대표적인 기법이다.

15. 하이퍼파라미터 튜닝이란 무엇인가?
=> 하이퍼파라미터란 데이터 과학자가 최적의 훈련 모델을 구현하기 위해 모델에 설정하는 외부 구성 변수이다. 개발자에 의해 수동으로 수정되지 않고 모델이 데이터로부터 학습하여 자동으로 설정되는 파라미터와 다르게, 하이퍼파라미터는 모델이 학습되기 전에 사람이 직접 설정해야 한다. 예시로 학습률, 에폭 수, 가중치 초기화 등이 있다. 
하이퍼파라미터 튜닝이란 모델의 성능을 높이기 위해 하이퍼파라미터 값을 조절하는 과정이다.

16. 결정트리에서 불순도(Impurity) – 지니 계수(Gini Index)란 무엇인가?
=> 결정트리에서 불순도란 노드 안에 다양한 클래스가 섞여 있는 정도를 말하며, 지니 계수는 이를 수치화한 지표로, 값이 작을수록 더 순수한 노드임을 의미한다.

17. 앙상블이란 무엇인가?
=> 앙상블이란 여러 개의 개별 모델을 조합하여 최적의 모델로 일반화하는 방법이다. 약한 모델(weak classifier) 들을 결합하여 강한 모델(strong classifier)을 만드는 것이다. 결정트리에서 과적합이 발생하는 문제를 앙상블을 통해 감소시킬 수 있다. 비용이 많이 든다는 단점이 존재한다. Random Forest는 앙상블의 일종이다.

18. 부트 스트랩핑(bootstraping)이란 무엇인가?
=> 머신러닝에는 Bootstrap은 원래의 데이터 셋으로부터 랜덤 샘플링을 통해 학습데이터(Training Data)를 늘리는 방법으로, 데이터 양을 늘릴 수 있고 분포를 고르게 만들 수 있는 효과를 보여준다. 통계적 추정이나 앙상블 기법(특히 배깅)에 활용된다. 중복을 허락하여 샘플링 하는 방식이다.

19. 배깅(Bagging)이란 무엇인가?
=> 배깅이란 여러 개의 모델을 각기 다른 데이터 샘플로 학습시켜 그 결과를 평균(회귀) 또는 다수결(분류)로 결합하는 앙상블 기법 중 하나이다. 그리고 모델을 서로 다른 데이터셋으로 학습시키기 위해 부트스트랩핑을 이용하여 여러 개의 데이터셋을 생성한다.

20. 주성분 분석(PCA) 이란 무엇인가?
=> PCA란 고차원 데이터를 더 낮은 차원으로 축소하면서 데이터의 정보를 최대한 보존하는 수학적 기법으로서, 많은 특성(feature) 중에 중요한 축만 골라 데이터를 작고 간단하게 표현하는 방법이다. 차원의 저주 극복, 보델 단순화, 노이즈 제거 등의 효과를 볼 수 있다. 여러 방향으로 퍼져있는 데이터에서 가장 정보가 많은 방향을 찾아 그 방향을 주성분으로 정하고 데이터를 이 주성분 축으로 회전 및 투영하여 차원을 줄이는 것이 PCA의 원리이다.
