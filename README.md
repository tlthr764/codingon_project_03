# 하스스톤 데이터 분석
-------------------------------------------------------------------------------------------------------------------------------
## 목차

1. 분석 목적
2. 프로젝트 진행 스케줄
3. 분석 과정
4. 분석 결과
-------------------------------------------------------------------------------------------------------------------------------
## 1. 분석 목적
- 오랜만에 하스스톤에 복귀했는데, 하스스톤의 현상태가 어떠한지 궁금증이 들었다. 
- 또한 전설 등급에 효율적으로 달성하기 위하여, 유저들이 어떤 직업을 많이 플레이하고 어떤 덱이 승률이 좋은가에 대한 메타 분석을 해보고 싶어 본 프로젝트를 시작하게 되었다.
-------------------------------------------------------------------------------------------------------------------------------
## 2. 프로젝트 진행 스케줄
<pre>
2023.11.21 : 프로젝트를 시작했다.
2023.11.23 : 데이터 분석 주제를 하스스톤으로 선정했다. 
             하스스톤 전설 등급 유저수를 데이터 크롤링하고 시각화했다.
2023.11.24 : 기간과 대상을 특정하여 직업별 점유율 데이터를 크롤링하는 코드를 짰다.
2023.11.25 : 직업별 점유율 데이터를 크롤링하고 시각화했다.
2023.11.26 : 덱별 대전 통계 크롤링 코드를 짜기 시작했다.
2023.11.27 : 덱별 대전 통계를 크롤링하고 시각화했다.
2023.11.28 : 프로젝트 발표 준비를 했다.
2023.11.29 : 발표 후 피드백을 받아서 수정할 부분을 정리했다.
2023.11.30 : data_legend.ipynb의 코드를 수정 및 주석 작업을 했다.
2023.12.01 : graph_legend.ipynb의 코드를 수정 및 주석 작업을 했다.
2023.12.06 : data_meta.ipynb의 코드를 수정 및 주석 작업을 했다.
2023.12.10 : graph_meta.ipynb의 코드를 수정 및 주석 작업을 했다.
2023.12.11 : graph_meta_().ipynb 파일들의 코드를 수정 및 주석 작업을 했다.
</pre>
-------------------------------------------------------------------------------------------------------------------------------
## 3. 분석 과정

### 분석 기준 :

#### 하스스톤 전설 유저수
- 기간 : 2022년 10월 ~ 2023년 11월
- 대상 : 현재 운영 중인 아시아, 유럽, 아메리카 서버에 존재하는 전설 등급 유저
- 전설 등급 달성을 위해서는 50% 이상의 승률과 일정한 게임수가 필요하므로, 시즌별 전설 유저수는 하스스톤의 흥행 척도라고 볼 수 있다.

#### 하스스톤 직업별 점유율
- 기간 : 2022년 11월 15일 ~ 2023년 11월 28일자
- 대상 : 전 서버에 존재하는 모든 등급 유저
- 서버별, 일별, 등급별로 직업 점유율이 어떻게 다른지 분석해보기로 했다.

#### 하스스톤 승률 통계
- 기간 : 2022년 11월 15일 ~ 2023년 11월 28일자
- 대상 : 전 서버에 존재하는 다이아, 전설, 상위 1000등 유저
- 등급별로 상세한 메타 분석과 데이터 필터링을 통해 나만의 맞춤형 데이터 분석을 해보기로 했다.

### 데이터 출처 :

- [순위표-하스스톤](https://hearthstone.blizzard.com/ko-kr/community/leaderboards/)
- [하스스톤 승률통계](https://hsreplay.net/)
  
### 분석 방법 : 

- 데이터 크롤링과 웹자동화를 통한 데이터 수집
- matplotlib와 seabron을 사용한 데이터 시각화
-------------------------------------------------------------------------------------------------------------------------------
## 4. 분석 결과

### 4-1. 하스스톤 전설 유저수
![하스스톤 전설 유저수 추이 (서버 총합)](https://github.com/tlthr764/codingon_project_03/assets/143565463/14251ff2-aef1-4b32-b716-20b0e323b382)
![하스스톤 전설 유저수 추이 (서버별)](https://github.com/tlthr764/codingon_project_03/assets/143565463/8bf0b582-137e-4ced-bdca-42a564ad2547)
![중국 서버 종료 전후 평균 전설 유저수 비교](https://github.com/tlthr764/codingon_project_03/assets/143565463/e447398c-18ef-4439-bfce-221e5f5c7226)
![중국 서버 종료 전후 전설 유저수 평균 비교 (서버별)](https://github.com/tlthr764/codingon_project_03/assets/143565463/ae3f80db-9002-4eb2-8031-7442a7631548)
![하스스톤 전설 유저수 추이 (월별)](https://github.com/tlthr764/codingon_project_03/assets/143565463/e5b3937d-356a-4808-825b-c3ebcab30eee)
![확장팩 발매 전후 전설 유저수 추이](https://github.com/tlthr764/codingon_project_03/assets/143565463/787db4b9-24aa-408d-9bad-4a16fa236194)
- 하스스톤 전설 유저수는 증가하는 추세이며, 최근 아시아 서버의 전설 유저수가 급격히 증가했다.
- 중국 서버가 종료된 이후, 서버 종료 이전보다 평균 전설 유저수가 증가한 것으로 보아 중국 유저들이 다른 서버로 유입되었다고 유추할 수 있다.
- 아시아 서버가 평균 전설 유저수 차이가 제일 큰 것으로 보아 중국 유저들이 아시아 서버에 가장 많이 유입되었을 것으로 추측할 수 있다.
- 확장팩 이전월보다 발매월의 전설 유저수가 증가한 것으로 보아 확장팩이 발매되면 유저의 유입이 증가한다는 것을 알 수 있다.

### 4-2. 하스스톤 직업별 점유율

#### 하스스톤 직업별 플레이 빈도 :
![하스스톤 직업별 플레이 빈도](https://github.com/tlthr764/codingon_project_03/assets/143565463/6984c2b3-1857-4f29-98c2-d5708cb15e8f)
- 죽음의기사, 성기사, 드루이드 3직업의 점유율 합이 전체 점유율의 1/3 이상을 차지한다.
- 마법사, 흑마법사, 전사 3직업이 각 10% 내외의 점유율을 차지한다.
- 주술사, 악마사냥꾼은 각 5% 미만의 점유율 차지한다.

#### 서버별 직업 분포도 :
![서버별 직업 분포도](https://github.com/tlthr764/codingon_project_03/assets/143565463/4b012b62-b0d4-4d72-9d26-f1bcec4e9d5e)
- 유럽, 아메리카 서버의 직업 점유율은 죽음의기사>성기사>드루이드 순을 보인다.
- 아시아 서버의 직업 점유율은 타 서버와 상이하게 성기사>죽음의기사>드루이드 순을 보인다.

#### 일별 직업 점유율 추이 :
![일별 직업 점유율 추이](https://github.com/tlthr764/codingon_project_03/assets/143565463/c0777e59-4553-4428-ab84-94ac4633098b)
- 마법사는 데이터 수집을 시작한 24일에 비해 마지막 수집일인 28일에 점유율이 상승하는 추세를 보인다. [10.4% > 11.4%]
- 드루이드는 24일에 비해 28일에 점유율이 하락하는 추세를 보인다. [11.3% > 9.9%]

#### 등급별 직업 점유율 추이 : 
![등급별 직업 점유율 추이](https://github.com/tlthr764/codingon_project_03/assets/143565463/d6472e45-f096-4200-b38f-a85c82922f10)
- 악마사냥꾼은 하위 랭크에서는 낮은 점유율을 보이나, 다이아 이상의 상위 랭크로 갈수록 점유율이 급격하게 증가하여 상위 1000등권에서는 직업 점유율 1위를 차지한다.
- 죽음의 기사는 하위 랭크에서는 높은 점유율을 보이나, 전설 이상의 상위 랭크로 갈수록 점유율이 급격하게 감소하여 상위 1000등권에서는 직업 점유율 하위권에 위치한다.

### 4-3. 하스스톤 승률 통계
![직업별 덱 유형별 점유율  모든 등급](https://github.com/tlthr764/codingon_project_03/assets/143565463/43f29176-25d2-49e3-b86b-56821777c78f)
![직업별 덱 유형별 점유율  다이아 등급](https://github.com/tlthr764/codingon_project_03/assets/143565463/3dd3bb00-7800-4f4e-8c4b-c7ba71f232fb)
![직업별 덱 유형별 점유율  전설 등급](https://github.com/tlthr764/codingon_project_03/assets/143565463/7b222d43-9834-498e-826a-ef9a6451eae6)
![직업별 덱 유형별 점유율  상위 1000 등](https://github.com/tlthr764/codingon_project_03/assets/143565463/c5a1bd2c-9528-4b90-b411-b7637c8b742c)
![덱별 대전 통계  모든 등급](https://github.com/tlthr764/codingon_project_03/assets/143565463/09d915ff-3876-4e7e-ac71-bbc2504430ba)
![덱별 대전 통계  다이아 등급](https://github.com/tlthr764/codingon_project_03/assets/143565463/0eae4a4d-efef-42a5-8ae8-309ea5deea01)
![덱별 대전 통계  전설 등급](https://github.com/tlthr764/codingon_project_03/assets/143565463/5fc09b0d-4dca-4af9-9e6d-e548971854f6)
![덱별 대전 통계  상위 1000 등](https://github.com/tlthr764/codingon_project_03/assets/143565463/38b5780f-be23-4c41-9b37-cab3feb3c77c)

#### 등급별 Review : 
- 등급이 높아질수록 평균 승률이 높은 덱과 낮은 덱 사이의 편차가 작아진다. 이를 통해 등급이 높아질수록 실력의 편차가 줄어든다고 유추할 수 있다.

#### 직업별 Review : 
1. 죽음의 기사
- 하위 랭크에서는 높은 점유율을 보이나, 점유율에 비해 낮은 승률을 보인다. 상위 랭크로 갈수록 점유율과 승률이 감소하는 것으로 보아 등급전에서 비효율적이라고 유추할 수 있다.
2. 성기사
- 전 랭크에 걸쳐 높은 점유율은 보이고, 평균 승률도 상위권에 위치한다. 다만 상위 랭크로 갈수록 승률이 조금 감소하는 것으로 보아 직업의 저점이 높지만, 고점은 높지 않다고 유추할 수 있다. 따라서 전설 등급 달성까지는 쓸만한 직업이라고 생각한다.
3. 드루이드
- 하위 랭크에서는 높은 점유율 보이나, 점유율에 비해 낮은 승률을 보인다. 특히 성기사와의 매치업에서 크게 낮은 승률을 보이는 것을 통해, 성기사에게 상성이 불리하여 상위 랭크로 갈수록 점유율이 낮아진다고 유추할 수 있다.
4. 마법사
- 전 랭크에 걸쳐 10% 내외의 꾸준한 점유율을 보이고, 평균 승률의 변화가 거의 없다. 이를 통해 직업 간의 상성을 잘 타지 않는 무난한 직업이라고 유추할 수 있다.
5. 악마사냥꾼
- 하위 랭크에서는 낮은 점유율을 보이나, 다이아 이상의 상위 랭크로 갈수록 점유율이 급격하게 증각하여 상위 1000등권 통계에서는 직업 점유율과 평균 승률이 최상위에 위치한 것으로 볼 수 있다. 따라서 사용하는 플레이어의 실력이 필요하지만, 고점이 높은 직업이라고 생각한다.
-------------------------------------------------------------------------------------------------------------------------------
