머신러닝 분류 문제에서의 혼동행렬

머신러닝의 분류(Classification) 문제에서는 모델의 성능을 평가하기 위해 혼동행렬(Confusion Matrix) 을 자주 사용한다. 혼동행렬은 모델이 예측한 값과 실제 값을 비교하여 어떤 예측이 맞았고 어떤 예측이 틀렸는지 시각적으로 보여주는 표이다.


---

혼동행렬의 기본 형태

이진 분류(Binary Classification) 문제를 기준으로 혼동행렬은 다음과 같은 형태를 가진다:

실제 클래스
                양성(Positive)   음성(Negative)
예측 양성  ->     TP               FP
예측 음성  ->     FN               TN

TP (True Positive): 실제 양성을 양성으로 정확히 예측한 경우

FP (False Positive): 실제는 음성이지만 양성으로 잘못 예측한 경우 (Type I error)

FN (False Negative): 실제는 양성이지만 음성으로 잘못 예측한 경우 (Type II error)

TN (True Negative): 실제 음성을 음성으로 정확히 예측한 경우



---

주요 평가 지표 (Confusion Matrix 기반)

혼동행렬을 기반으로 다양한 성능 지표를 계산할 수 있다. 대표적인 4가지는 다음과 같다:

1. 정밀도 (Precision)

정의: 양성으로 예측한 것들 중에서 실제 양성의 비율

공식:

Precision = TP / (TP + FP)

설명: 예측 결과 중에서 얼마나 정확히 양성을 골라냈는지를 의미한다. FP가 많으면 precision이 낮아진다.


2. 재현율 (Recall, Sensitivity, TPR)

정의: 실제 양성 중에서 모델이 양성이라고 올바르게 예측한 비율

공식:

Recall = TP / (TP + FN)

설명: 놓치지 않고 얼마나 잘 잡아내는지를 의미한다. FN이 많으면 recall이 낮아진다.


3. F1 점수 (F1 Score)

정의: 정밀도와 재현율의 조화 평균

공식:

F1 Score = 2 * (Precision * Recall) / (Precision + Recall)

설명: Precision과 Recall 사이의 균형을 고려한 지표. 두 값이 모두 높을 때 높은 F1 점수를 얻을 수 있다.


4. 정확도 (Accuracy)

정의: 전체 예측 중에서 맞게 예측한 비율

공식:

Accuracy = (TP + TN) / (TP + FP + FN + TN)

설명: 전체적으로 얼마나 잘 맞췄는지를 나타내는 지표. 클래스 불균형이 있을 경우 주의해서 사용해야 한다.



---

이러한 지표들을 종합적으로 활용하여 분류 모델의 성능을 다각도로 평가할 수 있다.

