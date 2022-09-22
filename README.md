# 철도 데이터분석 기획서

## 입지 선정
### PV
- 폐철도로 진행
- 장점
    - 기존에 많이 분석되지 않았다.
    - 어느정도 기본 분석 흐름은 정해져있다. (지역별 전력 소모량, 그에 대응하는 전력 수요량)
        - 폐철도의 위치를 같이 표시해서 필요한데 공급할 수 있다.
        - nrel에서 기본 입사량은 나옴
    - 한 지역에서 몰려있으면 전송하는데 이정도 비용이 드는데 철도와 같이 흩어져 있으면 그 비용을 절약할 수 있다
- 고려사항
    - 최종 사용자에게 전력을 전송하기 위해 송전 시설, 도로 시설, 상수도 및 기타 지역 기반 시설이 필요하다.
    - PV설치는 도시 성장에 영향을 줄 수 있으므로 주거 지역에서 최소 500m의 거리를 유지해야 한다

## 태양광 입지 발굴 기획서

### 국공유 유휴부지란?

국가에서 소유하거나 사용할 수 있는 쓰지 않는 땅을 의미합니다.

그 예시로는 폐철도, 폐항만, 폐교, 공공시설, 군사시설 이전 적지 등이 있습니다.

이에 저희가 설계한 전체적인  분석 시나리오는 아래와 같습니다. 기본적인 파이프라인은 전체 유휴부지 분석후 그 중 유리한 입지를 선정하고 그 입지 분석을 구체화하는게 원래 순서인데 현재 상황은 ①과 같이 주제가 대략적으로 정해진 상황이기 때문에 프로세스를 ②번과 ③번으로 나누어서 분석을 진행하였습니다.

<img width="717" alt="스크린샷 2022-06-24 오전 9 29 38" src="https://user-images.githubusercontent.com/62462552/175436794-659397f3-295e-4c6f-a6ef-534c472f15cc.png">

## 데이터
- 철도
    - [https://data.go.kr/data/15012349/fileData.do](https://data.go.kr/data/15012349/fileData.do)


# 1. 태양광 입지 관련 정보 종합 분석

1. 위치, 면적, 사용료, 일사량, 전력판매 형식, 설치비, 운영비

 - (1)과 (3)을 같이 보여주기 (실제 사용 가능한 면적을 보여주기 위해)

   - [ ]  **(지도)** (1) 국내 지도에서 **철도의 위치의 분포 찍기** (시도 경계를 기준으로 점 찍기)
       - geojson 파일을 Osmnx에 넣어서 그리기
   - [ ]  **(지도)** 국내 지도에서 철도의 밀집도 그림 그리기 (전체 도로를 기준으로)  
   - [ ]  **(지도)** nrel에서 **구간별 태양 입사량, 전력 생산량에 대한 정보** 시각화 
       - [ ]  **(지도)**구간별 입사량이 더 높은 곳을 진하게 표시해서 추가 시각화 (건한)
       - [ ]  **(표)** 구간별 전력 입사량에 대한 표 그리기 **(**지선**)**
   - [ ]  **(표)** nrel에서 받은 전력 생산량에 대한 정보를 바탕으로 구간별 수익 시각화 
   - [ ]  **(표)** 철도별 설치비용와 계산 후 시각화
       - 태양광 설치비용 데이터 이용 (구글 Sunroof 프로젝트)
       - [https://www.kaggle.com/datasets/jboysen/google-project-sunroof](https://www.kaggle.com/datasets/jboysen/google-project-sunroof)
   - [ ]  **(지도)** 국내 송신탑 위치 시각화
   - [ ]  **(지도)**국내 송신탑 위치와 철도의 위치를 같이 그리기 (단순히 위치만)
   - [ ]  **(지도)** 국내 **송신탑 위치와 철도 위치를 접근성을 표현**하는 그림 그리기
   - [ ]  **(표)** 전력 판매 비용과 운영비에 대한 내용 조사후 정리
   - [ ]  **(표)** 운영비와 접근성 그림을 엮어서 전국 폐철도에 설치시 높은 접근성을 시각화
![Untitled](https://user-images.githubusercontent.com/62462552/175525502-fdb7c2df-73a4-47c7-b98e-ebeb2aec8cb9.png)



# 2. 항공사진 및 수치지도 활용 적합 부지 확인

1. 적합한 철도 Top 10에 대해 분석하고 실제 사진과 함께 예시 보여주기
2. 그리고 여기 상위 10개의 철도에 대해서는 철도를 가상 시뮬레이션으로 태양광을 올린 이미지 들고와도 좋을 듯 (찾아보면 시각화 시뮬레이션 툴 많이 나옴)
   - [ ]  **(표)** 마지막으로 철도 Top10에 대해 10개의 입사량 선 긋기

        (각각의 선은 다른 철도를 나타내고 X축은 나눈 구간, Y축은 구간별 입사량)

   - [ ]  **(표)** 마지막으로 철도 Top10에 대해 10개의 생산 전력 선 긋기

        (각각의 선은 다른 철도를 나타내고 X축은 나눈 구간, Y축은 구간별 생산 전력)

   ![Untitled (1)](https://user-images.githubusercontent.com/62462552/175525539-945f3c23-0f7d-4ef9-8cd5-ee719807e31f.png)

   ![Untitled (2)](https://user-images.githubusercontent.com/62462552/175525562-5e411ad8-3dd1-4235-96ee-d290dba3220f.png)
 
   ![Untitled (3)](https://user-images.githubusercontent.com/62462552/175525558-8ca27f24-a3ee-4e50-92d9-fd85c3182e4c.png)



# 3. 터널 여부 고려는 미정

   - [ ]  (**(지도)** (3)국내 지도에서 터널을 고려한 사용가능한 철도의 위치 찍기)
   - [https://www.data.go.kr/data/15025445/standard.do](https://www.data.go.kr/data/15025445/standard.do)
   - [https://www.data.go.kr/data/15025445/standard.do](https://www.data.go.kr/data/15025445/standard.do)
   - // 철도에 터널 데이터

        [https://www.kric.go.kr/jsp/industry/rss/installlineList.jsp?q_fdate=2018](https://www.kric.go.kr/jsp/industry/rss/installlineList.jsp?q_fdate=2018)

   - 직접 지도에서 확인해야함
