Walking Kaggle Part3 소개
========================================================
author: Sang Yeol Lee
date: March 09 2018
width: 1600 
height: 1400
transition: linear
transition-speed: slow
autosize: true

========================================================
id: slide1
type: prompt

### 대상자 
  * **스터디는 취미 모임이기 때문에 참여는 누구나 가능, 다만 지속적으로 참여할 수 있는 분만** 
  * 다만 R 또는 Python 중에서 최소 1개 언어를 다룰 줄 아셔야 되고 머신러닝 기초가 있어야 참여하는데 어렵지 않음.
    - 언어를 다루지 못하고 머신러닝을 잘 모르시면 다른 스터디를 권유드립니다. ([싸이버스 참조](https://www.facebook.com/thepsybus))
  * 토요일 격주로 진행 (오전 10시 ~ 오후 1시)
    - 장소 : 서울특별시 마포구 월드컵북로 396 연구개발타워(R&D타워) 13층 공개SW개발자센터 상암(역량프라자)
    - 스터디 관련 공지는 페이스북 대화창 또는 캐글뽀개기 페이스북, 싸이버스

<br> 

### 주제 : 캐글 도전반 (정말.. 캐글을 뽀개봅시다)
  * 운영 지원: [캐글뽀개기](https://www.facebook.com/groups/kagglebreak) 
  * 장소 지원: [kosslab](https://kosslab.kr/)
  * [페북 이벤트 링크](https://www.facebook.com/events/357422671441392/)
    - 스터디 자료는 구글드라이브 또는 github을 통해서 관리할 예정입니다.
    - [github  주소](https://github.com/KaggleBreak/walkingkaggle)
    - [스터디 구글드라이브](https://drive.google.com/drive/folders/0B2l0iH28o85xSG83OTVfMzhhNFE?usp=sharing) 
    - [스터디 일정표](https://docs.google.com/spreadsheets/d/15OgrZKj6pD0jptFnkTIWioqC1_2_eoJidkysRXBlDyw/edit#gid=0)

========================================================
<br>

## Kaggle - https://www.kaggle.com

* Wikipedia - Kaggle?
  - Kaggle은 기업 및 연구원이 데이터 및 통계를 게시하고 데이터 마이너가 예측 및 설명을 위한 최상의 모델을 만들기 위해 경쟁하는 예측 모델링 및 분석 경쟁을위한 플랫폼. 
  - Crowdsourcing 접근 방식은 예측 모델링 작업에 적용 할 수있는 무수한 전략이 있으며 어떤 기술 또는 분석가가 가장 효과적인지를 처음부터 알 수 없다는 사실에 의존.


## 오늘 일정?
  * 스터디 소개 (10시~ 10시40분)
  * 쉬는 시간 (10시 40분 ~ 11시)
  * KKBox's Churn Prediction Challenge 대회 공유 (11시~11시40분)
  * 쉬는 시간 (11시 40분 ~ 11시50분)
  * 조 구성하기 (11시 50분 ~ )
  * 종료

<br>

## 자료참고 레퍼런스
  [General Tips for participating Kaggle Competitions, Mark Peng, Taiwan Kaggle Master](https://www.slideshare.net/markpeng/general-tips-for-participating-kaggle-competitions) 


***
<div align="center">
<img src="./img/part3.jpg" width=900 height=900></div>

========================================================
## 2단계 : 일반적인 캐글 접근방법(1)
[Go to slide 1](#/slide1)
<div align="left">
<img src="./img/img_1.png" width=800 height=600></div>

* 일반적인 캐글의 데이터 셋은 Train set, Test Set으로 나뉨 (Submission 파일이 따로 있음)

* Test Set은 대회 기간 동안 제출하면 채점 용도로 공개되어 있는 Public LB(Leardboard)와 대회 끝난 후 최종 채점을 평가하는 Private LB(Leardboard)가 있음

* 물론 데이터 셋이 일반적이지 않을 수 있음
  - 대회의 목적(상금, 직업, 지식 공유...)에 따라서 문제가 달라짐.


========================================================
## 2단계 : 일반적인 캐글 접근방법(2)
<div align="left">
<img src="./img/img_2.png" width=1000 height=800></div>

- 캐글 프로세스는 데이터 분석의 절차 (서비스의 직접 반영하진 않지만, 커뮤니케이션은 포럼의 참가자들과 Kernel에서 Notebook 형태로 공유)

- 1단계 데이터 전처리, 2단계 싱글 모델, 3단계 변수 구성, 4단계 탐색적 자료 분석, 5단계 다양한 모델 구성, 6단계 앙상블, 7단계 예측

========================================================
## 2단계 : 일반적인 캐글 접근방법(3)

* 데이터 전처리 
    - 데이터를 (로컬 혹은 서버)에서 읽을 수 있는 사이즈인지? (메모리, 하드) 
    - 데이터의 마이그레이션은 어떻게 할 수 있는지?
    - 변수로 구성할 수 있는 데이터와 구성할 수 없는 데이터가 무엇에 있는지?

<br>

* 싱글 모델
    - 기본으로 대회에서 제공한 변수 기준으로 1차 모델을 구성

<br>

* 변수 구성
    - Submission ID의 추가할 수 있는 변수가 어떤 것이 있을까?
    - 변수 선택, 차원 축소, 중요한 변수 확인 (모델 기반)
    - Single 모델 별로 유용한 변수를 추리는 것. 모델에 걸리는 시간 고려
    - 텍스트 또는 카테고리 변수는 어떻게 활용할 것인지?
    
<br>
    
* 탐색적 자료 분석
    - 변수들의 데이터의 분포는 어떻게 되는지? (단변량)
    - 변수들간의 관계는 어떻게 되는지? (다변량)
    - 이상치는 어떻게 확인하고 어떤 조치를 취할 수 있는지? 
    - 데이터 정규화
    - 어떤 변수를 더 추가할 수 있는지 아이디어 또는 인사이트 발견
    

========================================================
## 2단계 : 일반적인 캐글 접근방법(4)

* 다양한 모델 구성
    - 문제가 회귀, 분류, 추천 어떤 것을 목적으로 삼고 있는지에 따라 모델 구성이 다름
    - (분류) 로지스틱 회귀모형, Tree 모델, Bayesian 모델, 신경망 모델, Kernel 모델 등 구성 하여 모델 간의 결과 값 기반하여 상관관계 파악
    - 모델들의 다양한 파라미터를 어떻게 구성할 것인지?
        - 파라미터 별로 성능 파악 (조합), 또는 일반적으로 구성하는 파라미터를 디폴트로 구성

<br>

* 앙상블
    - 블랜딩 작업 (모델에서 나오는 결과 값들의 평균을 가지고 예측할 것인지? 아니면 가중치?)
    - 모델 결과들의 값들을 합쳐서 다시금 부스팅으로 학습
    - Public의 제출하면서 다시금 파라미터 또는 모델을 조정하면서 학습
   
<br>

* 제출
    - Submission.csv 파일로 예측 결과를 데이터로 제출.
    - 문제에 따라 제출 형태도 다르고 평가 방식도 다름.
    - 클래스의 확률로 제출하거나, 클래스의 값을 제출하거나, 여러 개의 값 (상위 5개)를 제출하거나
    - 평가 방식 F1 Score, Logloss... [https://en.wikipedia.org/wiki/Precision_and_recall]
    

========================================================
## 2단계 : 일반적인 캐글 접근방법(5)

- precision : 맞다고 예측 한 것 중에 실제로 정답이 얼마나 되나?  $${\displaystyle \mathrm {PPV} ={\frac {\mathrm {TP} }{\mathrm {TP} +\mathrm {FP} }}}$$
- sensitivity : or Recall, 맞는 케이스에 대해 얼마나 많이 맞다고 실제로 예측했나?, $${\displaystyle \mathrm {TPR} ={\frac {\mathrm {TP} }{P}}={\frac {\mathrm {TP} }{\mathrm {TP} +\mathrm {FN} }}}$$

- 숫자 인식 문제에서 “5-detector”로 binary class 문제를 맞춘다고 한다면 제일 왼쪽 부분에서 threshold를 결정하게 되면(오른쪽은 5, 왼쪽은 5가 아님) True 5를 잘 맞추게 됨. 그래서 True 5 모두 다 5라고 예측함. 다만 Precision 측면에서 5라고 주장한 것중에서(전체 8개)에서 2개가 틀리게 되어 75%(2, 6)
- 중앙 부분에서 threshold를 결정하게 되면 Recall은 67% (True 5 중에서 2개를 놓치게 됨), Precision 측면에서는 5라고 주장한 것중에서 1개만 틀려서 80%.
- 제일 오른쪽 부분에서 threshold를 결정하게 되면 Recall은 50% (True 5중에서 3개를 놓치게 됨), Precision 측면에서 5라고 주장한 것중에서 하나도 틀리지 않아 100%

<div align="left">
<img src="./img/img_5.png" width=1200 height=600></div>

========================================================
## 2단계 : 일반적인 캐글 접근방법(6)

<div align="left">
<img src="./img/img_3.png" width=800 height=600></div>


- [Bias-Variance Tradeoff Wikipedia](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff)

### Bias? 
- Bias는 학습 알고리즘에서 잘못된 가정으로 부터 나오는 에러
- High Bias - Low Variance / Underfitting , 몸무게 = Beta 0 + 키 * Beta1 일거야.

### Variance?
- Variance는 훈련 데이터 내의 작은 변동에 대한 민감성으로부터 나오는 에러이다. 높은 variance는 의도한(일반화) 학습결과를 내기보다는 훈련 데이터 내의 무작위 소음을 모델링함에 따라 과적합을 야기한다
- Low Bias - High Variance / Overfitting , 몸무게 = Beta 0 + 키 * Beta1 + 키^2 * Beta2 + 키^3 * Beta3... + 키^8 + Beta8  일거야.

- 어떤 모델이든 Underfitting 하거나 Overfitting 할 수 있음, 적정선을 찾아야 함. 주로 Train 데이터를 Validaton 하여 해당 에러와 Test 에러를 같이 확인, Test Error를 보기 전에 평가 함수를 구성하여 Validation Error를 확인하는 것이 핵심! (Cross Validation, Local CV)
    

========================================================
## 2단계 : 일반적인 캐글 접근방법(7)

<div align="left">
<img src="./img/img_4.png" width=800 height=600></div>

- K-Fold Cross Validation (K=5)

- 균일하게 K 갯수만큼 Train 데이터를 쪼갬. k=5이면 5개로 쪼개서, Round 1~5번까지 Train data의 80%를 모델 구성하는데 사용하고 20%를 Validation 하는 데 사용, 해당 작업을 5번 거쳐서 평균 cv를 구하여 모델을 평가

- local CV와 Public LB 간의 갭 차이가 나는 K를 찾는 것이 팁. 데이터가 Imbalance 되어 있다면 Stratified K-fold cv(목표변수의 클래스 비율을 똑같이 구성하여 쪼개는 방법)를 구성하라고 추천하고 있음

- [Stratified K-fold cv, scikit-learn](http://scikit-learn.org/stable/modules/generated/sklearn.model_selection.StratifiedKFold.html)

========================================================
## 3단계 : 조 구성하기 (1)
[Go to slide 1](#/slide1)

[워킹캐글 파트3 설문지](https://docs.google.com/forms/d/e/1FAIpQLSdOsLzZ8yGLOkLl27f5i4v9W1vvrn2feLMxS461vB-6WEuw6Q/viewanalytics)

### 사용하는 주 언어는 무엇입니까?
- 파트2 비율 -> 파트3 비율
- R 사용자 (약 31.7% -> 41.7%)
- Python 사용자 (약 58.3% -> 58.3%)


### 캐글 대회에 참여한 횟수?
- 0회 (약 65% -> 58.3%)
- 1회 (약 20% -> 19.4%)
- 2회 (약 6.7% -> 11.1%)
- 3~4회 (약 5% -> 5.6%)
- 5회 이상 (약 3.3% -> 5.6%)


### 하는 일은 무엇입니까?
- 직장인 (약 50% -> 52.8%)
- 대학생 (약 28.3% -> 19.4%)
- 대학원생 (약 6.7% -> 11.1%)
- 취업준비생 (약 15% -> 16.7%)


========================================================
## 3단계 : 조 구성하기 (2)

### [스터디 참가자 행동강령, 꼭 지켜주세요](https://www.facebook.com/groups/kagglebreak/permalink/1967162913538381/)

### 발표 원칙
* 조별로 최소 1개 대회를 진행하고 캐글뽀개기 스터디 내에서 공유하는 것 
  - 중간 발표의 원칙
    (조 별로 자유롭게 내용 선정하여 발표, Ex. 데이터 전처리, 탐색적 데이터 분석, 싱글 모델까지만 진행)
  - 최종 발표의 원칙
    (조 별로 발표 날까지의 제출 기준으로 내용을 참가자들에게 공유)
  - 발표 시간은 중간, 최종 약 20~40 분 정도
  - (추가) Kaggle Kernel Notebook 작성   (Ex) [윤선미님의 캐글 competition 참가한 노트북](https://www.kaggle.com/sunmiyoon/one-hour-analysis-written-in-both-eng-and-kor)


<br>

### 주제 
* 이번 스터디에는 총 N개 대회 진행 예정(일반 대회 N개, 튜토리얼 대회 1개)

* 튜토리얼 대회 제외한 일반 2개 대회에서 Public LB 또는 Private LB가 가장 높은 팀 2팀 선정
  - 가장 높은 2팀 전원에게는 상금(데이터 분석 관련 책 전달) 예정, (참가자들에게 필요한 비용은 추후 공지드리겠습니다)

* 튜토리얼 대회는 [부동산 가격 문제](https://www.kaggle.com/c/house-prices-advanced-regression-techniques) 또는 [타이타닉 문제](https://www.kaggle.com/c/titanic#tutorials) 대회 중에서 진행하며 처음 캐글에 참여하는 분들은 해당 대회로 시작하길 권장합니다 :)

========================================================
## 3단계 : 조 구성하기 (3)

### 조별 진행방법
* 조는 참여 주제 / 사용 언어에 따라서 구성하려고 합니다, 같은 조 내에서는 되도록 1개 언어를 사용할 것을 권장함
  - 조별로 참여하기 부담스러운 분은 개인으로 참여해도 됩니다, 다만 다른 조처럼 공유/발표를 똑같이 해야합니다.

* 조별, 개인으로 참여하기 어려운 분은 스터디 참여를 되도록 권장하진 않습니다.

* 조별로 스케줄은 알아서 정합니다(오프라인, 온라인), 스케줄은 진행하는 조장이 정하는 것으로 합니다.

* 조별로 역할 분담은 알아서 정함. 역할 분담도 진행하는 조장이 정하는 것으로 합니다.
* 토요일 격주로 만날 때는 발표 내용만 공유하는 것으로 합니다

========================================================
## 3단계 : 조 구성하기 (4)

### Q&A?
* 개별로 모여서 진행할 때에는 장소 지원이 되나요?
  - 되도록 지원드릴려고 하지만 어려울 수 있습니다. 다만 모이실 때 사진 공유도 페이스북 그룹 통해서 해주시면 감사드립니다.

* 참여할 수 있는 시간이 애매한데 어떻게 해야될까요?
  - 직장인 분들도 많기 때문에 시간이 서로 잘 안나서 진행이 원활하게 안되는 것이 사실입니다. 한 분이 혼자서 하게 될 가능성이 높은데 같이 서로 알려주면서 할 수 있으면 좋겠고 그래서 캐글을 처음 접하는 분들은 튜토리얼을 먼저 진행하는 것을 권장합니다. 대회 진행 하실 때 여유있게 하는 것을 목표로 합니다. 조별로 최소 한 ~ 두달 정도 시간을 드릴 예정입니다.

* 자료는 어떻게 공유하면 되나요?
  - github 또는 구글드라이브로 주제 별 폴더를 만들테니 해당 폴더에 자료를 올려주세요. github 권한 드리겠습니다.

* 커뮤니케이션은 어떻게 하면 될까요?
  - 조별로 자유롭게 하시면 됩니다.

* 잘 모르는데 참여해도 될까요?
  - 캐글을 잘 모르면 우선 튜토리얼부터 하시죠! 그리고 모든 대회 마찬가지만 목표는 커널에 있는 코드들을 이해하여 리뷰하고 공유하는 것도 좋은 발표 자료일 수 있습니다. 

*  스터디 참여하다가 불가피하게 시간이 안되면 어떻게 할까요?
  - 조장님에게 연락주시고, 조장님이 힘들면 발표 스케줄은 조정 가능하니깐 저에게 연락주세요~

========================================================
## 3단계 : 조 구성하기 (5)

### 일반 대회

* 후보 주제(1)
: [Google Cloud & NCAA® ML Competition 2018 Men](https://www.kaggle.com/c/mens-machine-learning-competition-2018)
  - Kagglers는 과거의 토너먼트 결과를 바탕으로 모델을 제작하고 테스트합니다.두 번째 단계에서 경쟁 업체는 2018년 NCAA Division I Men's 및 Women 's Basketball Championships에서 가능한 모든 경기의 결과를 예측합니다. 첫 번째 단계는 모델 구축에 대한 인센티브를 제공하고 예측을 평가할 수있는 수단을 제공합니다. 실제 경쟁은 2018 년의 결과를 예측합니다.
  - Stage 1 - Model Building (~Mar 10), LogLoss, [Evalution](https://www.kaggle.com/c/mens-machine-learning-competition-2018#evaluation)
  
* 후보 주제(2)
: [TalkingData AdTracking Fraud Detection Challenge](https://www.kaggle.com/c/talkingdata-adtracking-fraud-detection)
  - 하루에 30 억 회의 클릭을 처리하며, 그 중 90 %가 잠재적으로 사기성이 있습니다. 클릭 사기를 방지하는 방법은 포트폴리오에서 사용자의 클릭 경로를 측정하고 많은 클릭을 발생시키는 IP 주소를 신고하지만 결코 앱 설치를 중단하지 않는 것입니다. 2 차 경쟁에서 모바일 앱 광고를 클릭 한 후 사용자가 앱을 다운로드할지 여부를 예측하는 알고리즘을 작성해야합니다. 
  - May 7, 2018, ROC Curve, [Evalution](https://www.kaggle.com/c/talkingdata-adtracking-fraud-detection#evaluation) 

* 후보 주제(3)
: [Toxic Comment Classification Challenge](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge)
  - 온라인에서 학대와 괴롭힘의 위협은 많은 사람들이 자신을 표현하지 않고 다른 의견을 찾는 것을 포기하는 것을 의미합니다. 초점 영역은 독성적인 코멘트(부정적인 온라인 행동)을 연구하는 것입니다. Perspective의 현재 모델보다 위협, 외설, 모욕, 신원 기반 혐오와 같은 다른 유형의 독성을 탐지 할 수있는 모델을 구축해야합니다. 
  - Entry deadline March 13, 2018, LogLoss, [Evalution](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge#evaluation)  
  
  
* 후보 주제(4)
: [Google Landmark Recognition Challenge](https://www.kaggle.com/c/landmark-recognition-challenge/data)
  - 이미지 픽셀에서 직접랜드 마크 레이블을 예측하여 사람들이 사진 컬렉션을 더 잘 이해하고 구성 할 수 있도록 도와줍니다. 까다로운 테스트 이미지의 데이터 세트에서 올바른 랜드 마크를 인식하는 모델을 작성하도록 요구합니다. 이 과제는 Landmark Retrieval Challenge (https://www.kaggle.com/c/landmark-retrieval-challenge)와 함께 구성됩니다. 특히, 두 도전 과제 모두에 대한 시험 세트는 참가자들이 두 가지 모두에서 경쟁하도록 권장한다는 점에 유의하십시오. 
  - May 15, 2018 - Entry deadline, LogLoss, [Evalution](https://www.kaggle.com/c/landmark-recognition-challenge#evaluation)  
  

========================================================
## 3단계 : 조 구성하기 (6)
### 튜토리얼

- 튜토리얼 주제(1)
: [부동산 가격 문제](https://www.kaggle.com/c/house-prices-advanced-regression-techniques) 

- 튜토리얼 문제(2)
: [타이타닉 문제](https://www.kaggle.com/c/titanic#tutorials)

========================================================
## 3단계 : 조 구성하기 (7)
[Go to slide 1](#/slide1)

### - 조 구성하기

### - 조별 스케줄 짜기


==================
# The End

- 원래 스터디 격주인데.. 장소 사정 상 2회차 모임은 3/31일 날 진행하겠니다.
- 대신 오늘 이후로 각 조별로 모임 진행해주세요!!
- 조장님들은 발표 스케줄 선정하겠습니다.
