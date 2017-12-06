---
title: "강의 커리"
layout: post
author: songhunhwa
---

### 목적
분석 실무에서 접하는 다양한 문제를 이해하고 직접 해결해보는 경험을 통해 실무 역량을 제고한다.   
일반적으로 분석 프로세스는 아래와 같다.  
- *문제 정의 및 가설 수립*
- *데이터 설계 및 수집/처리/검수*
- *데이터 추출 및 전처리*
- *통계 분석 or 모델링 및 평가*

분석 업무에 필요한 기술적/이론적 내용과 더불어, 아래 나열된 소프트 스킬을 획득하여 전달력과 효과성을 높인다.  
- *분석가로서 마인드셋/태도 등*
- *커뮤니케이션 방식, 보고서 작성법 등*

### 강의특성  
본 강의는 실무에 쓰이는 프로그래밍과 실용적인 이론을 중심으로, 수업의 효과를 극대화하기 위한 커리큘럼으로 구성되었다.   
만약 아래 지식 및 스킬을 사전에 보유하고 있을 경우, 강의를 쉽게 이해할 수 있으며 효과성을 높일 수 있다.  
- *Python(for문, if문, lambda함수, 슬라이싱 등)을 통해 원하는 형태의 데이터셋을 만들 수 있음*
- *Numpy, Pandas, Scipy, Statsmodel, Scikit-learn, Matplotlib 등의 라이브러리 사용법을 알고 있음*
- *통계 및 머신러닝에 대한 기초 지식을 보유하고 있다. (ANOVA, Regression, RandomForest, SVM 등의 목적과 설명이 가능함*
- *SQL(Hive or Presto) 쿼리를 작성하여 간단한 전처리를 할수 있음*

위에 나열된 사전 지식/스킬이 필수는 아니지만, 대략적인 개념과 기초가 부족할 경우 강의 내용을 이해하는 데 어려움이 있을 수 있다. 강의에 대한 문의는 <songhunhwa@gmail.com>으로 자유롭게 진행 가능하다.

### 커리큘럼
강의 커리큘럼은 총 8회로 진행되며, 5회의 강의/실습과 3회의 프로젝트로 진행된다. 상황에 따라 일부 내용은 변동될 수 있다.

#### [1강 Part 1: 분석실무에 대한 이해](https://songhunhwa.github.io/2017/10/24/da-python-concept.html)
- 분석 주제 예시
- 분석 프로세스
- 팀구성 및 역할
- 분석툴 및 환경 소개
- 소프트 스킬/역량
	
#### [1강 Part 2: 데이터 수집 및 처리 시스템 소개](https://songhunhwa.github.io/2017/11/16/da-python-intro_p2.html)
- Apache Spark & Modules 소개
- 클라이언트 로그 설계 사례 
- (실습)Json 및 Text 형태의 로그 데이터 Parsing
- (실습)SQL 및 Numpy, Pandas를 통한 전처리 
	
#### [2강: 유저 Funnel 분석을 통해 이탈 구간 개선](https://songhunhwa.github.io/2017/12/05/da-python-funnel.html)  
- 문제 정의 및 가설 정립
- 분석 Frame 구성
- 데이터 로딩 및 전처리
- 탐색적 데이터 분석 / 클러스터링
- 시각화 및 리포팅

#### 3강: 랭킹 및 추천 로직 Prototype 구축
- 문제 정의 및 가설 수립
	- 랭킹과 추천을 위한 목적 정의
	- 모델 효과 측정을 위한 지표 산출
- 데이터 추출 및 전처리
	- Pandas로 CSV 데이터 읽기
	- 데이터셋 준비하기
- Popularity-based model
	- 변수 선정 및 데이터셋 준비
	- Score 산출 및 정렬	
	- 클릭율 예측 모델(Regression)을 통한 랭킹 로직 생성
	- 로직 평가 및 개선
- Collarborative Filtering
	- 데이터셋 준비
	- Neighbor, MF 기반 모델 생성
	- 모델 평가 및 개선
		
#### 4강: 신규 비즈니스 지표 개발 (이탈 위험 지표)
- 유저 이탈 방지를 위한 Risk Indicator 정의
	- Key Risk Indicator란?
- 변수 생성 및 전처리
	- 데이터셋 읽기 및 전처리
	- EDA 및 Bounce 기준 정하기
	- Regression의 회귀계수로 지표 생성하기
- 웹 대시보드 구축
	- Re:dash란?
	- Re:dash로 대시보드를 구축하기
- Statesmodel을 이용한 시계열 예측
	- 지표의 흐름을 예측해보자
		
#### 5강: 결제 예측 모델을 통한 결제율 제고
- 문제 정의 및 목적
	- 결제 가능성이 높은 집단의 특성을 파악하고 예측하는 모델 생성
- 데이터 추출 및 준비
	- 변수 선정 및 전처리
- 모델 구축 및 평가
	- Scikit-learn의 Pipeline 기능을 이용해 Classification 모델 생성하기
	- 오버피팅 이슈 해결(K-fold), 하이퍼파라메터 튜닝하기 (GridSearch)      
	- Scikit-learn.Evaluation 모듈을 통해 모델 평가/개선하기  
		
#### 6~8강: 개별 프로젝트**  
- 개별 프로젝트 진행 및 피드백
- 프로젝트 결과 발표