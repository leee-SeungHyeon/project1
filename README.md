## 냉동 컨테이너 BIGDATA/AI 기반 고장예지보전 서비스 플랫폼 개발/사업화
<hr>

### Purpose
- 실제상황에서는 예기치 못한 고장으로 인해 데이터를 수집하지 못할 가능성이 존재
- 고장에 영향을 주는 주요 변수를 선택하고 나머지 변수는 차원을 축소하여 고장 예측

### Role
- 현업 담당자 인터뷰 및 실제 컨테이너 데이터 레이블링 작업
- 실제 냉동 컨테이너 데이터 전처리
- 기계학습 모델 조사 및 모델링
- 비지도 학습 모델 모델링

### Process
<img src="https://user-images.githubusercontent.com/123627186/232266389-c0f9cbe7-9855-4135-9ecd-628fdd57d42a.png" width="450" height="400">

### Data
-  111개의 실제 냉동 컨테이너 뽑아낸 총 63개 특성을 가지고 있는 운영 데이터(1시간마다 특성값이 기록됨)
- 시뮬레이션 냉동 컨테이너 데이터

### Data Preprocessing
![image](https://user-images.githubusercontent.com/123627186/232266526-2f3e9791-cb7f-4eb1-9908-eb3ae1926e12.png)

### Method
- Extreme Gradient Boosting
- Decision Tree
- Random Forest
- Light Gradient Boosting
- Principal Component Analysis

### Result
<img src="https://user-images.githubusercontent.com/123627186/232266694-c4c1d362-193e-4a68-ba97-368d8bd2c035.png" width="550" height="400">

### Conclusion
- 각 모델별로 고장에 주요한 영향을 미치는 변수들을 찾아 냈음
- 기존의 지도학습 방법만 사용하는것에 비해 Key Feature + PCA 사용하는 방법의 성능이 크게 향상되었음
- Key Feature + PCA 방법 사용시 부스팅 계열의 XGB 모델과 LGBM 모델의 Recall 값은 0.62, 0.72로 기존의 방법보다 각각 0.36, 0.39씩 상승한 결과를 보였음

### Output
- 논문 : PCA 및 변수 중요도를 활용한 냉동컨테이너 고장 탐지 방법론 비교 연구(KCI, 1저자)
