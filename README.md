LOL 15분 데이터 기반으로 승패 결정 요인 중요도 파악
========================================
### 패스트캠퍼스 DSS 14기
팀구성 : 강동윤(DSS 14기), 김형기(DSS 14기)

데이터 사이언스 14기 첫 번째 프로젝트의 일환으로, 데이터 분석의 기초가 되는 EDA(데이터 전처리) 과정을 리그 오브 레전드라는 게임의 특성 및 수치를 통해 학습하고자 한다.

GOAL
-------------------------------------
Challenger 등급 게임의 15분 데이터 승/패에 영향을 미친 요인과 entire duration 게임의 요인들과 비교하여 얼마나 달라지는 지를 파악하는 것을 목표로 한다.

Preparation 및 데이터 출처
-------------------------------------
1. Kaggle의 League Of Legends Challenger Rank Game-10min,15min(https://www.kaggle.com/gyejr95/league-of-legends-challenger-rank-game10min15min)의 데이터를 참조
2. Kaggle의 League Of Legends High elo Ranked Games(2020)(https://www.kaggle.com/gyejr95/league-of-legends-challenger-ranked-games2020)의 데이터를 참조
3. 2개의 데이터를 jupyter notebook으로 불러온 이후, pandas DataFrame으로 데이터 전처리를 시작한다.

Execution
-------------------------------------
1. 첫 번째 데이터(Challenger_Ranked_Games_15minute.csv):
  이상치 제거 -> 컬럼 간 상관계수 -> 필요없는 컬럼 전처리(Diff 컬럼 생성) -> 상관관계 파악 및 시각화 -> Feature_importances
2. 두 번째 데이터(Challenger_Ranked_Games.csv):
  이상치 제거 -> 컬럼 간 상관계수 -> 필요없는 컬럼 전처리(Diff 컬럼 생성) -> 상관관계 파악 및 시각화 -> Feature_importances

Detail
-------------------------------------
### Programing Language:
- Python 3.7(Anaconda Jupyter Notebook)

### 결론 & 한계점
#### 결론
- 
