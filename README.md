# 체력 측정 평가를 통한 운동 추천 서비스  

### 주제 선정 이유

 코로나로 인한 건강에 대한 관심이 증가함에 따라 홈 트레이닝에 대한 관심를 바탕으로 운동에 대한 흥미를 촉진 시키는 서비스 제공



### 프로젝트 개요

- 국민 체력 100 에서 활용하고 있는 체력 측정 데이터를 활용

- 클러스터링을 활용하여 운동 추천과 영상을 제공하여 이용자 편의를 고려한 서비스 개발



### 프로젝트 기간

2021.10.6~2021.11.12



### 프로젝트 진행 과정

(데이터 수집 --> 데이터 전처리 및 피처선별 --> 데이터 모델링 -->웹 서비스 --> 결론 및 향후 과제)



#### 1. 프로젝트 구성도

- 프로젝트 구성도를 바탕으로 프로젝트 진행

![image](https://user-images.githubusercontent.com/98143525/157196544-cb2c9865-96d1-4f05-b011-8dfbb08d3857.png)



#### 2. 데이터 수집

- 국민 체력 100에서 체력 측정에 관한 데이터 수집

​	![image](https://user-images.githubusercontent.com/98143525/157223608-1223a375-020d-4ff5-89ee-78c39ca1be4d.png)

- 운동정보와 영상 데이터 크롤링

​	![image](https://user-images.githubusercontent.com/98143525/157223816-b50c1b63-70da-4796-9137-6246533be2c5.png)

- 데이터 적재 및 처리(운동 데이터)

​	![image](https://user-images.githubusercontent.com/98143525/157224059-00fc4fd8-b0ad-471f-824c-5458bf3f66e0.png)

- 데이터 적재 및 처리(체력 측정 데이터)

​	![image](https://user-images.githubusercontent.com/98143525/157224258-9bcdc968-cf8d-4506-9959-0b8f0ba460d4.png)

#### 3. 데이터 전처리

- 국민 체력 100에서 체력 측정 기준 항목을 바탕으로
- 수집한 데이터에서 필요한 피처 선별

​	![image](https://user-images.githubusercontent.com/98143525/157224707-59796934-3c78-4857-8115-cc483c3cfa26.png)

- 전처리를 위한 피처를 선택하고
- 데이터 라벨링 및 결측치 제거 작업(필요없는 컬럼 삭제)
- IQR Rule을 활용하여 이상치 제거

​	![image](https://user-images.githubusercontent.com/98143525/157224951-5a1b60d1-5477-44d9-845e-38929cb32659.png)



#### 4. 데이터 모델링

- Elbow Curve 와 실루엣 계수를 사용하여 k 값을 찾아 내어 클러스터링 값 도출

​	![image](https://user-images.githubusercontent.com/98143525/157225528-50fefcec-e1c8-4d55-9d63-7810a3cb2c49.png)

- 군집 별 특성 데이터를 바탕으로 처방 데이터 라벨링

​	![image](https://user-images.githubusercontent.com/98143525/157226498-c2d8262e-20df-4e93-b856-6a7af6c54213.png)



-  도메인 지식을 활용하여 실제 군집에 대한 운동 처방

​	![image](https://user-images.githubusercontent.com/98143525/157226213-04928882-97e1-45b9-8da6-a89ccff0f1a8.png)

#### 5. 웹 서비스 구현

- 웹 페이지 기능 설명
- 최종 프로젝트 파일에 영상 시연 파일 참고

​	![image](https://user-images.githubusercontent.com/98143525/157227241-d5e91cac-d7ab-4e22-a444-6f9eb4331bd8.png)

#### 6. 결론 및 향후 과제

- 전문가의 지식을 기반한 서비스를 무료로 사용 가능
- 언택트 시대에 홈 트레이닝 수요 급증에 따라 여러 기기에 호환 가능성 증가
- 티처블 머신의 모델 학습 정확도 한계에 따른 운동 측정의 제약
- 비슷한 서비스가 존재하고 사용자 데이터 검증의 어려움
- 폭발적인 성장이 기대되는 가장 IT 헬스케어 시장에서 누구나 이용 가능한 서비스로 확장
