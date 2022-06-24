# 철도 데이터분석 기획서

# 1. 태양광 입지 관련 정보 종합 분석

1. 위치, 면적, 사용료, 일사량, 전력판매 형식, 설치비, 운영비

 - (1)과 (3)을 같이 보여주기 (실제 사용 가능한 면적을 보여주기 위해)

   - [ ]  **(지도)** (1) 국내 지도에서 **철도의 위치의 분포 찍기** (시도 경계를 기준으로 점 찍기)
       - geojson 파일을 Osmnx에 넣어서 그리기
   - [ ]  **(지도)** 국내 지도에서 철도의 밀집도 그림 그리기 (전체 도로를 기준으로)  (1)
   - [ ]  **(지도)** nrel에서 **구간별 태양 입사량, 전력 생산량에 대한 정보** 시각화 (건한)
       - [ ]  **(지도)**구간별 입사량이 더 높은 곳을 진하게 표시해서 추가 시각화 (건한)
       - [ ]  **(표)** 구간별 전력 입사량에 대한 표 그리기 **(**지선**)**
   - [ ]  **(표)** nrel에서 받은 전력 생산량에 대한 정보를 바탕으로 구간별 수익 시각화 (지선)
   - [ ]  **(표)** 철도별 설치비용와 계산 후 시각화 (지선)
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

   - 직접 지도에서 확인해야할수도
