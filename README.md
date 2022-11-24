# NICE DNB & NUMBLE <비재무 데이터를 활용한 중소기업 휴폐업 예측 챌린지

### 제공된 데이터
* 액티브 중소법인 재무보유: (28,982개 데이터, 28개 변수)
* 휴폐업 중소법인 재무보유: (6,739개 데이터, 28개 변수)
* 재무데이터: (109,142개 데이터, 76개 변수)

### EDA 및 전처리
* 결측치 제거
* 라벨링(휴폐업: 0, 액티브: 1)
* 모든 변수 7가지 구간으로 Binning(이상치 처리 및 모델링을 위한 전처리)
* 설립일자와 상장일자 업력으로 변경
* 파생변수 생성(총 24개)

### 모델링
* 변수 전처리
  * 1차 필터링) Binning된 변수 구간별 부도율 시각화하여 그래프가 상승 또는 하강 추세일 때 모델링 변수로 선택
  ![image](https://user-images.githubusercontent.com/65642065/203484868-5e359309-70b4-4106-ae1c-711c4a042581.png)
  
  
  
  * 2차 필터링) 단변량 분석으로 유의미한 변수 선정



    ![image](https://user-images.githubusercontent.com/65642065/203485136-978eae82-46c0-408a-890d-74e452eb0f1a.png)
    
* 모델링
 * 앙상블을 통해 모델 구축
   
   
   ![image](https://user-images.githubusercontent.com/65642065/203697705-dfecff07-8026-475b-b72a-653c56b1d325.png)
 * 비재무데이터 결합한 모델
   
   
   ![image](https://user-images.githubusercontent.com/65642065/203697796-d18517c4-2331-4a3f-907b-b7c2b00933a4.png)


