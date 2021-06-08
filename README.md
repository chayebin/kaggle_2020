### <Kaggle 데이터분석 주택가격 예측(분류)>
​
​
# 0. 목차 
> [1. 목적](#1-목적)  
> [2. 프로젝트](#2-프로젝트)   
> [3. 모델](#3-모델)    
> [4. 결론](#4-결론)

​
​
# 1. 목적  
> * 데이터 전처리와 훈련 모델 선택으로 높은 정확도 도출
> * 머신러닝에 대한 이해도 향상

​
​
# 2. 프로젝트
### 2.1. 프로젝트 소개
> * Kaggle 데이터분석 주택가격 예측(분류) 경진대회
> * 2020.07.03 ~ 2020.08.31(348H) - 캐글 프로젝트는 일주일동안 진행
> * 해외 주택 구조와 관련된 79개의 데이터를 바탕으로 조사와 토론을 통해 주택 가격에 영향을 주는 데이터를 선별하고, 선별된 데이터의 결측치를 채우고, 변수를 생성하고, 인코딩을 하는 절차를 걸쳐 최적의 머신러닝 모델을 통해 높은 정확도를 도출

​
​
### 2.2. 프로젝트 진행 과정
> 1. 데이터 해석
>    * 수치형(모든 정보를 이상적인 숫자로 표현하는 변수) ex) 12.245, 215.15, ...
>    * 범주형(개별 항목으로 구분되는 데이터값을 갖는 변수) ex)높음, 낮음, 중간, ...
>    
> 2. 데이터 전처리
>    * 이상치 제거
>    * 결측치 확인(범주형은 'NA'로 채움, 수치형은 범주화 후 가장 높은 비율의 값으로 채움, 관련 없거나 결측치가 많은 데이터는 제거)
>    * 데이터 분류(재산, 외관, 크기, 벽난로, 난방, 차고, 욕실, 지하실, 베란다로 분류)
>    * 데이터 생성(크기와 관련된 데이터를 더해 '집의 총 면적' 생성, 각 층 별 욕조의 개수를 더해 '총 욕조 수' 생성, ...
>    * 인코딩(문자형을 숫자형으로 변환) ex)높음 = 0, 중간 = 1, 낮음 = 2
>    
> 3. 최적의 모델 탐색
>    * LinearRegression
>    * KNeighbor
>    * GradientBoost
>    * Rasso
>    * Ada
>    
> 4. 예측한 결과 CSV 파일로 저장

​
​
### 2.3. 개발 환경
> * 툴 : Anaconda – Jupyter Notebook   
> * 언어 : Python(Pandas, Numpy, Sklearn, Seaborn)

​
​ 
# 3. 모델
### 예측값 시각화
* LinearRegression   
![image](https://user-images.githubusercontent.com/82797757/121130689-b9d81700-c869-11eb-90cd-3e41385cb7e6.png)
* KNeighbor   
![image](https://user-images.githubusercontent.com/82797757/121130698-bc3a7100-c869-11eb-9d51-704825c0335d.png)
* GradientBoost   
![image](https://user-images.githubusercontent.com/82797757/121130705-be043480-c869-11eb-95c2-ff23d1ae3c46.png)
* Rasso   
![image](https://user-images.githubusercontent.com/82797757/121130712-bfcdf800-c869-11eb-8306-ac514bf338bb.png)
* Ada   
![image](https://user-images.githubusercontent.com/82797757/121130716-c0ff2500-c869-11eb-84ff-c4a4f3524395.png)

​
​ 
# 4. 결론 
### 이상치가 가장 적은 GradientBoost로 선택   
~~~
훈련 근사도   : 0.9947476369136521   
테스트 근사도 : 0.9670562785160219   
~~~
### 캐글 경진 대회에서 우수상 수상
![image](https://user-images.githubusercontent.com/82797757/121131666-138d1100-c86b-11eb-94c1-a0c07b7d1008.png)

