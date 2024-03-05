## 총선 후보 관련 기사와 테마주 간 상관분석

### 1. 연구목적 및 배경

- 2024 총선을 앞두고 각 정당의 예비 후보자들에 대한 관심이 높아지고 있음
- 특정 정치인 선정 (한동훈)
- 그에 관한 뉴스 기사를 분석하며, 함께 묶인 '테마주'에 관심
- 정치인에 대한 대중과 여론의 반응이 긍정적인지, 부정적 인지에 따른 그의 테마주 가치 변화 분석
- 이를 통해 테마주 가격에 변동을 주는 요인이 무엇인지 파악 할 수 있고, 투자에 도움이 될 것으로 예상

### 2. 데이터 수집/분석 방법

- 네이버 뉴스 기사 크롤링(2023년 1년간 데이터)
- 감성사전 library 활용
- 한동훈 관련 테마주 3곳 선정(오파스넷, 태양금속우, 디티앤씨)

- 수집된 뉴스기사 감성분석 -> 감성 score값 매김
- 도출된 score값과 주가 간의 상관분석 진행

-> 감성 사전을 통해 긍정적인 단어에는 +1점 or +2점 부과/ 부정적인 단어에는 -1점 or -2점 부과, 점수 합산

### 3. 데이터 분석 과정

- 각 뉴스기사별로 감성 score 값을 매긴 후 양수면 긍정, 음수면 부정적인 뉴스 기사로 판단
- 각 날짜별로 긍정적인 뉴스 기사 개수 - 부정적인 뉴스 기사 개수 = 그날의 최종 감성 score

#### 주가 데이터 전처리
주가 데이터의 중요한 시계열적 특징 2가지: 최근에 접어들수록 스케일이 커짐/자기상관성
 - 대부분 주식은 과거에 비해 주가가 크게 상승 : 과거의 1%보다 현재의 1%의 등락폭이 더 크다!
 - 오늘의 가격 정보는 전날 가격 정보와 가장 밀접한 연관이 있고 상관계수가 매우 높음
 - 스케일 변화 무시 : log변환 / 자기상관성 무시 : 오늘 종가 – 전날 종가 (차분)


- 주가 데이터와 뉴스기사의 감성 score 단위 통일하기 위해 정규화 수행 ->그래프로 시각화
- 최종적인 피어슨 상관계수 값 도출


### 4. 결과 분석 및 최종 결론

- 태양금속우/오파스넷 : 상관관계가 음수로 도출
- 디티앤씨 : 근소하지만 양의 상관관계
- 전체적으로 봤을 때 상관관계가 거의 존재 X
- 원인?
   - 뉴스 기사 감성 score가 대부분 부정적인 값
   - 정치 기사에 부정적인 단어가 많이 포함
   - 해당 정치인 관련 뉴스만 보고 주식을 사지는 않음 -> 다양한 요인
 
- 그러나..
  - 11/20~11/30 기간에 대해서는 어느 정도 상관관계가 보임
  - “ 한동훈이 총선에 출마할 가능성 높다 “ 라는 내용의 기사가 대거 쏟아짐 ⇒ 기대감에 매수
 
- 결론
   - 특정 정치인에 초점을 맞춘 기사
만으로는 주식시장에 큰 영향을
끼치지 않지만, 주요 이슈가 등장
하여 언론이 이를 집중적으로 다룰 경우, 주가에 유의미한 영향이
발생할 수 있다.
