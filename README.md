# 도로 통행량 시계열 예측 모델

2nd team project ft.yeardream

- 2022.02.16 - 2022.02.22
- with Kim TJ, Ahn CH, Choi HJ

### 문제 정의

- 35개 도로의 시간별 교통량 데이터를 학습, 이를 기반으로 미래의 교통량을 예측하는 과제

### 추진 배경

- 도시화, 밀집화에 따른 교통 혼잡도 예측의 중요성 증대
- 자율 주행 고도화 및 효율화를 위한 전제 조건

### 평가 지표

### RMSE(Root Mean Square Error)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/fc5c1c28-6a84-4652-9fe7-04c3cd87e6d1/Untitled.png)

- 예측 오차의 제곱합을 산술평균한 값의 제곱근
- 최종 점수는 Private 100%로 평가 (Public 미반영)

---

# 데이터 구조

- `train.csv` : 35개 도로의 2020.01.01 ~ 05.17 기간에 대한 도로 통행량 데이터
- `validation.csv` : 35개 도로의 2020.05.11 ~ 05.24 기간에 대한 도로 통행량 데이터
- `test.csv` : 35개 도로의 2020.05.18 ~ 05.31 기간에 대한 도로 통행량 데이터
(35개 도로의 ID가 column명으로 들어가 있음)
- 35개 도로의 2020.01 ~ 2020.05.24 기간에 대한 도로 데이터가 주어진 상태에서 35개 도로의 2020.05.25 ~ 2020.0531 기간에 대한 도로 데이터를 예측해야함  (필요에 따라 **데이터를 합해 train / validation 기간 재설정** 가능)
    
    ![train.csv](https://user-images.githubusercontent.com/99028164/154083372-376deffe-e6b9-4182-9c40-32f8dcaada3d.png)
    
    train.csv
    
    - 고속도로 코드와 명칭 매핑
        
        [제목 없음](https://www.notion.so/10059701e96e47b29c0c70faed1f6bb4)
        

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/00637ba0-c122-43e9-a4a0-c6541d90af2b/Untitled.png)
