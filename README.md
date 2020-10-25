LOL 15분 데이터 기반으로 승패 결정 요인 중요도 파악
========================================
### 패스트캠퍼스 DSS 14기
팀구성 : 강동윤(DSS 14기), 김형기(DSS 14기)

데이터 사이언스 14기 첫 번째 프로젝트의 일환으로, 데이터 분석의 기초가 되는 *EDA(데이터 전처리)* 과정을 리그 오브 레전드라는 게임의 특성 및 수치를 통해 학습하고자 한다.

GOAL
-------------------------------------
Challenger 등급 게임의 15분 데이터 승/패에 영향을 미친 요인과 entire duration 게임의 요인들과 비교하여 얼마나 달라지는 지를 파악하는 것을 목표로 한다.

Preparation 및 데이터 출처
-------------------------------------
1. Kaggle의 League Of Legends Challenger Rank Game-10min,15min(https://www.kaggle.com/gyejr95/league-of-legends-challenger-rank-game10min15min)의 데이터를 참조
2. Kaggle의 League Of Legends High elo Ranked Games(2020)(https://www.kaggle.com/gyejr95/league-of-legends-challenger-ranked-games2020)의 데이터를 참조
3. 2개의 데이터를 jupyter notebook으로 불러온 이후, pandas DataFrame으로 데이터 전처리를 시작한다.

Process
-------------------------------------
1. 첫 번째 데이터(Challenger_Ranked_Games_15minute.csv):
  null값 확인 및 이상치 제거 -> 컬럼 간 상관계수 -> 필요없는 컬럼 전처리(Diff 컬럼 생성)
2. 두 번째 데이터(Challenger_Ranked_Games.csv):
  null값 확인 및 이상치 제거 -> 컬럼 간 상관계수 -> 필요없는 컬럼 전처리(Diff 컬럼 생성)
3. 항목간 상관관계 분석:
<img width="984" alt="스크린샷 2020-10-25 오후 4 39 50" src="https://user-images.githubusercontent.com/65877745/97101461-f000c600-16e0-11eb-8fd5-cdb23f6953c6.png">
4. 두 데이터 (15분, 전체 게임 셋)의 컬럼 중요도 비교:
<div>
  <img width="219" alt="15분 게임" src="https://user-images.githubusercontent.com/65877745/97101496-4e2da900-16e1-11eb-9b86-e80df07b2621.png">
  <img width="215" alt="전체 게임" src="https://user-images.githubusercontent.com/65877745/97101499-52f25d00-16e1-11eb-8b33-77550c50faf3.png">
</div>

Conclusion
-------------------------------------
### 결론 & 한계점

1. 높은 티어의 플레이어들은 잘하면 잘 할수록 안정적으로 플레이하는 성향을 가지고 있다. 리스크를 동반한 변수를 만드는 것에 집중하기 보다, 상대방의 실수를 포착하였을 때 그것을 우리 팀으로 유리하게 가져오는 플레이 위주로 하며, 승률을 높인다.

2. 전체 게임 셋에서 게임 시간이 길어질수록 오브젝트도 더 많이 챙길 수 있기 때문에 둘의 결정관계지수가 높을 것이라 예상하였으나, 오브젝트들마다의 결정관계가 달라서 확인할 수가 없었다.

3. AOS 게임의 특성상 승/패에 가장 영향을 미치는 게이머의 실력, 다양한 챔피언 조합으로 생길 수 있는 변수, 아이템에 따른 변수들을 정량적 데이터로 구할 수 없다는 점에서 결론을 내리고, 그 다음 step으로 넘어가기에 부족하다는 결론을 내리게 되었다.
 
### Programing Language:
- Python 3.7(Anaconda Jupyter Notebook)
