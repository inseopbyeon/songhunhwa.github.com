---
title: "1회차 Part1: 분석 실무에 대한 이해"
layout: post
author: songhunhwa
---

### 목적
- 분석 실무의 예시와 주요 개념, 프로세스 전반과 세부 업무별 중요 사항에 대해 이해한다.
- 분석가의 업무 환경와 팀구조를 이해하고, 협업의 중요성을 인지한다.   
- 문제 정의 및 커뮤니케이션 등 소프트 역량/스킬의 역량을 높인다.

### 목차
1. 분석 주제 예시
2. 분석 프로세스
3. 팀구성 및 역할
4. 분석툴 및 환경 소개
5. 소프트 역량
6. 마치며

### 1. 분석 주제 예시

#### 데이터 분석이 제공할 수 있는 가치
데이터 분석가가 자주 다루는 **문제**는 어떠한 것이 있을까? 사실 데이터 분석 자체가 목적이 되는 경우는 '거의' 없다고 봐도 무방하다. 만약 데이터 분석이 목적이 되는 경우, 이미 문제가 있는 상황이거나 앞으로 생길 가능성이 높다.
데이터 분석은 데이터를 통해서만 만들어낼 수 있는 가치 혹은 서비스를 제공하기 위한 과정에 불과하다. 그렇다면, 데이터 분석이 어떠한 가치나 서비스를 만들어내는 데 기여할 수 있을까?    

일반적인 IT 회사의 경우 사업 영역을 간단하게 **1)비즈니스 영역, 2)개발 영역**으로 나눌 수 있다(실제 훨씬 복잡하다). 간단히 말해서, IT 회사는 서비스를 개발(생산)하고 이것을 통해 비즈니스를 하면서 소비자로부터 매출을 발생시킨다. 데이터는 이 과정에서 유요한 도움을 제공할 수 있다. (물론 데이터를 잘 이용한다는 가정 하에)

<img src="/img/lecture/it_concept.png" width="50%">

이제 각 영역별로 데이터가 제공할수 있는 가치/서비스에 대해 살펴보자

#### 기획/UX 영역
기획/UX 영역에서 가장 중요한 것은 유저에게 매끈한 경험을 제공하는 것이다. 매끈한 유저 경험이란? 데이터를 기반으로 해석할 때 Conversion Rate이 높다는 것을 의미한다. Converion Rate(전환율)은 Churn Rate(이탈율)의 반대어다. 즉, Churn Rate = 1 - Conversion Rate 이다.   
   
보통 Conversion Rate은 [Funnel 분석](https://en.wikipedia.org/wiki/Funnel_analysis)을 통해 파악한다(비록 오래된 방법론이긴 하지만 결과를 직관적으로 이해하기 쉽다). 이탈이 많이 일어나는 구간(Bottleneck)을 파악해 개선함으로써 향상된 UX을 제공할 수 있다. 개선을 위해 A/B Test가 주로 활용된다.

<img src="/img/lecture/funnel.png">

UX 개선뿐만 아니라, 데이터에 기반해 새로운 서비스를 기획하는 것도 가능하다. 대표적으로 아래 서비스가 상용화되어 있다.
- 추천/랭킹 서비스 (영화, 매장, 뉴스/블로그 컨텐츠, 아이템, 지인 등)
- 이미지, 텍스트, 오디오 데이터 처리를 통한 자동분류 서비스 (병 진단, 번역, 주문 처리 등)

또한 도메인 특성에 따라 다양한 목적으로 머신러닝의 Regression, Classification 기법이 활용된다. 예를 들면, 어뷰징 탐지나 채권 상환 여부 예측을 위해 Classification 모델을 만들며, 클릭율 예측을 위해 Regression 모델이 활용된다.       

#### 마케팅 영역
기본적으로 마케팅 부서는 돈을 쓴다. 따라서 ROI(Return on Investment)에 민감하며, KPI로 고려되는 경우가 많다. ROI는 Input 대비 Output을 계산한후 산출하며, 최소의 Input으로 Ouput을 극대화하는 것이 마케팅의 핵심이다. 기본적인 지표는 아래와 같다.    
- 집행량(expense) 대비 노출(impression)
- 노출 대비 클릭 (Click Thorugh Rate) 
- 클릭 대비 구매 (Purchase Rate)
- 구매 대비 재구매 (Repurchase Rate)
- 위 지표 역시 일종의 Funnel 분석이며, Segment별 성과를 측정할 수 있다.

<img src="/img/lecture/roi.png">

위 지표를 세그먼트별로 구분하거나 유입 채널별로 구분하는 등 다양한 관점으로 효과를 분석하고 마케팅 활동을 개선할 수 있다. 주로 사용하는 분석 방법은 회귀분석(Regression)이다. 이 경우, 실수 예측보다는 인과관계 파악하고 마케팅 Mix를 위해 이용한다. 
[마케팅 Mix](http://www.smartinsights.com/digital-marketing-strategy/online-marketing-mix/7ps-marketing-mix-alternative/)는 최적의 채널별 예산안 분배를 위한 분석으로, 채널별 Expense(원인, X)와 클릭율(결과, Y)이 필수 요인이다.   
   
마찬가지로, [STP](https://ko.wikipedia.org/wiki/STP_%EB%A7%88%EC%BC%80%ED%8C%85)(Segment, Targeting, Positioning) 전략 수립을 위해 데이터 분석이 활용되기도 한다. K-means 등의 클러스터링을 통해 전체 고객을 나누고 특정 기준(예, 충성도, 재구매율)으로 세그먼트를 정렬한 후 우선순위에 따라 맞춤형 컨텐츠/커뮤니케이션을 제공하여(Association-Rules), 마케팅 활동의 효율성/효과성을 높인다.    

<img src="/img/lecture/stp.png">

Source: [Logical Fox](https://www.logicalfox.com/blog/what-it-means-to-niche-down-and-how-to-do-it)

> A group of individuals or organisations sharing one or more similar characteristics that cause them to have relatively similar product needs and buying characteristics
— Dibb et. al.

#### 영업/CS/개발 영역
영업 영역에서는 신규 고객 창출과 기존 고객의 유지가 주요한 관심사이다. 데이터를 통해 신규 고객을 창출할 수 있는 기회/영역을 탐색할 수 있으며, 고객의 이탈을 사전 예측함으로써 이탈을 예방할 수 있다. CS 영역에서는 자동화 응대나 이슈 대응을 위해 데이터를 활용할 수 있다. 개발 영역에서는 제품의 안정화 및 버그 관리 등을 위해 데이터가 활용된다.    

### 2. 분석 프로세스
일반적인 데이터 분석의 업무 프로세스는 아래와 같다. 그러나 상황에 따라 유동적으로 바뀌는 경우도 많다. 각 단계가 모두 중요하지만 특히 프로세스의 처음과 끝의 중요성은 간과되지 말아야 한다. 문제 정의 및 리포팅 단계는 특별한 이론이나 스킬이 요구되지 않지만, 분석가의 경험과 태도, 일에 대한 철학에 의해 성과가 좌우되는 경향이 있다. 성공적인 프로젝트 진행을 위해 분석가는 필수 스킬/이론 뿐아니라 소프트역량을 지속적으로 개선해야 한다.

<img src="/img/lecture/process.png">

#### 문제 정의
업무의 큰 방향성과 전반적인 Frame을 설정하는 '문제 정의' 단계는 중요성을 아무리 강조해도 지나침이 없다. 유관자와 업무의 **목적, 이유, 비즈니스에 미치는 영향, 구체적인 설계와 지표, 일정과 예상 Output** 등에 대해 협의하는 단계에 해당한다. 분석가는 요청자의 모호한 비즈니스적 요구사항을 해석하고 구체화하여, 데이터 엔지니어와 협업을 통해 분석을 준비한다.    
   
이 과정에서 분석가는 요청자의 모호한 언어를 개발적인 언어로 해석할 수 있는 능력이 요구되며, 때로는 요청자의 니즈를 파악하여 문제 정의 과정을 리딩할 필요가 종종 발생한다. 또 구체화 과정에서 약간의 수학적 지식과 지표의 타당성을 고려할 필요가 있으며, 비즈니스와 연결성을 고려하여 전반적인 Frame을 잘 설정할 필요가 있다.   

<img src="/img/lecture/framework.png">

#### 데이터 수집
데이터 수집 및 처리 영역은 사실 데이터 엔지니어의 역할이 큰 비중을 차지한다. 최근 유저의 행동 패턴을 파악하기 위해 로그를 수집하는 경우가 많다. 일반적인 로그 데이터 수집/처리 과정은 아래와 같다. 로그성 데이터가 아닌 DB의 경우 별도 서버에 동기화를 하거나 이관하는 방식으로 마트를 구성한다.

- 로그 설계 단계
	- 로그 항목 및 Format 정의
	- Key, Value, Params 정의
- 모듈화 단계 
	- 모듈화 개발
	- 모듈 적용/테스트
- 로그 검증
	- 데이터 퀄리티 검증/관리
	- 수집 과정 모니터링

위 과정에서 분석가는 주로 로그 설계와 검증 부분을 담당한다. 분석 목적에 맞춰 무수한 로그를 선별하고 항목을 정의하며, 실제 데이터가 정의한 대로 잘 쌓이고 있는지 확인하고 수정하는 작업에 관여한다.

#### 데이터 처리
엔지니어가 담당하는 데이터 처리와 분석가가 진행하는 데이터 처리는 차이가 다소 있다. 엔지니어는 주로 실시간 혹은 시간대별 배치 작업을 통해 테이블을 업데이트하거나 동기화하는 업무를 맡는다. 이러한 작업 덕분에 분석가는 원하는 데이터를 추출하여 분석전 전처리 작업을 진행할 수 있다. 분석가의 입장에서 전처리 작업은 아래와 같은 활동을 의미한다.

- 데이터 추출, 필터링, 그룹핑, 조인 등 (SQL)
- 이상치 제거, 분포 변환, 표준화, 카테고리화, 차원 축소 등 (Python/R)

첫번째 항목의 경우 주로 SQL을 활용하며, 다양한 소스(DB, Hadoop 등)로부터 데이터 분석을 위한 기본적인 테이블을 만드는 단계이다. 이 단계에서 가장 중요한 점은 테이블과 컬럼의 명칭, 처리/집계 기준, 조인시 데이터 증식 방지 등이며, 데이터 엔지니어로부터 도움이 필요한 경우가 많다.    
     
두번째 항목의 경우, 데이터 분석가가 주도적으로 R이나 Python으로 진행하는 경우가 많으며, 의미 있는 분석 결과나 성능 좋은 모델을 만들기 위해 가장 중요한 단계라 할 수 있다. 대부분의 분석가는 이 과정에서 많은 시간을 소요하며, 모델 개선이나 재분석 진행시 이 과정으로 돌아와서 개선을 하는 경우가 많다.    

#### 데이터 분석
분석 영역은 사실 매우 큰 영역을 아우르는 범위이며, 도메인과 여러 상황에 따라 다양한 분석을 진행한다. 간략하게 영역을 구분하면 아래와 같다. (하지만 엄밀히 구분되는 개념들은 아니다)

- 지표 정의 및 트래킹
	- 비즈니스와 관련한 주요 지표를 개발/산출하고 대시보드 및 리포트를 통해 트래킹
	- DAU, MAU, WAU, NRU, Retention, Conversion(Purchase) Rate, ARPPU, LTV 등
- 통계분석
	- 모수 추정, 가설 검증
	- 변수간 관계 파악 및 변수간 영향력 파악
	- 통계 모형 구축
- 머신러닝
	- 분류 및 회귀 문제 해결
	- 추천 및 이상치 탐지 등
	- 이미지, 텍스트 등 비정형 데이터 처리/분석
 
<img src="/img/lecture/ds.png" width="60%">

Source: [Science2knowledge](https://science2knowledge.wordpress.com/data-science-scientists/)

#### 리포팅 및 피드백 반영
분석 결과 및 인사이트를 설들력 있게 정리/전달하는 과정이다. 아무리 좋은 분석 결과를 도출했다하더라도 이 단계가 제대로 진행되지 않으면 그 효과가 반감된다. 아래 나열된 원칙이 효과적이고 설득력 있는 전달을 하는 데 유용하다.
- **내용의 초점은 분석가 아닌 상대방**
	- 상대가 이해할 수 있는 언어 사용
	- 상대의 입장과 니즈에 맞춰 생각하고 결과를 정리
	- 목적을 수시로 상기하고 재확인
	- 분석 과정 보다는 '결과' 중심으로 전달
- **간결하고 명확한 메시지로 전달**
	- 짧은 문장 (불필요한 수식어 제거)
	- 블랙포인트 방식
	- 핵심 내용 먼저 전달후 근거를 나열
- **적절한 시각화 방법 활용**
	- 항목간 비교시 원 그래프는 지양하고 막대 그래프 위주
	- 시계열은 라인으로(실선)
	- 분포는 히스토그램이나 박스플롯
	- 변수간 관계는 산점도
- **투명하고 공정한 피드백**
	- 사실 기반 공유/보고
	- 실패를 두려하지 말것
	- 빠르고 적극적인 대응

### 3. 팀구성 및 역할
데이터사이언스팀은 크게 엔지니링과 분석 파트로 구분되며, 서로 협업을 통해 프로젝트를 진행하는 경우가 많다. 엔지니어와 분석가는 보유 역량 및 지식의 영역이 다르기 때문의 원활한 커뮤니케이션과 협업의 중요성, 목적의 공유가 특히 더 강조된다.

<img src="/img/lecture/ds_structure.png" width="60%">

#### 데이터 엔지니어
소프트웨어 개발에 대한 경험과 전문성을 보유하고 있으며, 시스템 환경(Spark, Hadoop) 설치 및 관리, 테이블 동기화/자동화 작업 등의 업무를 주로 맡는다. 주로 Scalar, Java, Python 등의 언어를 사용하며, 경우에 따라 웹/앱/서버 개발을 진행하기도 한다.

#### 데이터 분석가
로그 설계 및 지표 정의, 데이터 탐색 분석/모델링 업무를 맡는다. 통계/수학이나 산업공학을 전공한 경우가 많으며, 경영/마케팅, 사회/심리, 물리 등 다양한 전공자들이 데이터 분석 업무를 수행한다. 한 분야의 전문성과 지식으로 복잡한 현상을 분석하고 해석하기에 한계가 있으므로 여러 관점을 통해 다각적이고 풍부하게 해석하고자 하는 의지가 반영된 결과라 볼 수 있다.     
    
SQL(Presto, Hive)을 통해 데이터를 추출하여 로컬 머신에서 R/Python/사용툴을 사용해 분석하거나, 분산처리 환경인 경우 Spark가 제공하는  API(R/Python/SQL)를 이용해 분석한다. Adhoc이 아닌 트래킹이 필요한 경우 대시보드를 구축하기도 한다.    

### 4. 분석 툴 및 환경
분석 환경 및 시스템은 회사와 팀의 고유한 특성 및 상황에 따라 크게 좌지우지되는 경향이 있다. 일반적으로 IT 회사의 경우, 오픈소스 및 신기술에 대한 관심도가 높을 가능성이 있다. 반면에 보안에 민감하거나 보수적인 산업의 기업들은(예, 제조, 금융) 전통성 있고 상용 소프트웨어를 선호하는 경향이 있다. 단, 항상 예외는 있다. 보수적인 IT 회사도 존재하며 유연한 사고의 금융, 제조 회사도 존재한다.    
    
분석 환경 및 시스템의 실제적인 구축과 관리는 엔지니어의 역할이다. 다르게 이야기 하면, 이들의 도움 없이는 분석가 자체적으로 데이터를 추출/처리/분석하기에는 많은 어려움이 따른다. 또, 엔지니어가 구축한 환경에 분석가가 적응하지 못하면 분석 업무를 수행하는 데 문제를 경험할 수 있다.
이제 IT 회사를 예시로 분석 환경/시스템에 대해 간단히 살펴보자.      
- Spark (오픈 소스)
	- Java로만 다룰 수 있는 Hadoop을 보다 분석 친화적으로 개선 (Scalar, Python, R API 제공)
	- RDD, DataFrame, Dataset 등 다양하고 처리가 빠른 데이터셋 제공
	- RDD를 이용할 경우 데이터 I/O 작업을 디스크가 아닌 RAM 이용 가능
	- Lazy execution으로 보다 효율적인 작업이 가능
	- 다양한 분석 라이브러리 사용 가능(MLlibrary 등)
- Zeppelin (오픈 소스)
	- Rstudio, Jupyter Notebook과 유사한 역할
	- 코드를 저장하고 데이터를 시각화
	- 간단한 시각화/대시보드 제공
- 상용 툴
	- 엑셀, 태블로, 스팟파이어, 스플렁크, Re:dash
	- 구글 애널리틱스, 파이어베이스
	- SPSS, SAS, Matlab
- 분석 환경 예시

<img src="/img/lecture/tools.png">

### 5. 소프트 역량
#### 문제 정의
분석 프로세스의 첫 단계는 **문제 정의**이다. 이 단계에서 첫단추를 어떻게 맞추는가에 따라 프로젝트의 성패가 갈리는 경우가 많다. 문제의 정의를 잘 하기 위해서는 특정 지식이나 스킬 보다, 도메인 및 분석 경험이 더 중요하게 요구된다. 문제를 정의할 때 아래 나열된 항목을 고려하여 정의를 진행하는 것이 필요하다.
- 충분한 시간을 투자해 유관자와 논의/협의
- 변경사항 여부에 대해 지속적인 공유
- 많은 질문/대답을 통해 요구사항 명확화
- 문서화를 통한 기록
- 비즈니스에 미치는 영향력 고려하여 우선수위 산정
- 지표의 타당성과 신뢰성 확보

데이터 분석을 진행할 때 분석가는 많은 유혹을 느낀다. 시간을 더 투자해서 주제에 대해 깊게 들어가보고 싶고, 여러 방법론을 적용하면서 모델의 성능을 높이거나 풍부한 결과를 내고자 하는 생각을 가지게 된다. 그러나 현실적인 시간 제한으로, 적당한 깊이에서 분석을 중단하고 공유하는 것이 현명하다. (적당한 깊이에 대한 판단은 상황과 경험에 따라 매우 다양할 수 있다)    
    
또, 분석을 진행하다 보면 목적성을 상실하고 분석 행위 자체에 의미를 두는 경우도 있다. 이때 주요한 나침반의 역할을 하는 것이 초기에 정의한 분석 목적이다. 문서화 등을 통해 분석 진행중 상시로 확인하면서 배가 산으로 가는 일을 방지하는 것이 중요하다. 예를 들면, 코드를 쓰는 편집기에 목적을 간단히 기입하는 것도 유용한 방법이다.

<img src="/img/lecture/compass.png" width="40%">

#### 프레임 설정
데이터 분석 프로젝트를 시작할 때, (내용이 비어 있는) 틀(프레임)을 짜고 추후에 데이터 분석을 통해 내용을 채워 넣는 방식으로 진행하는 것이 효율적이다. 이는  잘못된 방향으로 혹은 너무 큰 범위로 분석이 진행되는 것으로 예방해준다. 더불어, 예상 내용을 미리 추측하고 각 결과에 따른 대응 방안을 미리 예상해두면 예상하지 못한 결과에 대해 당황하지 않고 적절한 인사이트를 도출할 수 있다. 프레임을 설정할 때 아래 원칙을 고려하면 도움이 된다.
- 문제 해결에 도달하기 위한 세부적인 주제/질문 선정
- 세부 주제별 필요 데이터 및 분석 방법론 정리
- 예상 Output 및 일정 산출
- 유관자 혹은 유관팀 정리

#### 태도 및 커뮤니케이션
대부분의 데이터 분석 프로젝트는 분석가와 엔지니어, 유관자가 협업하며 진행한다. 분석가는 데이터 탐색 및 모델링 등 상황에 맞는 방법론을 통해 결과를 도출하는 역할을 맡을 뿐, 실제 행동이나 변화를 일으키는 주체는 아니다. 주로 유관자가 결과를 수용해, 기존의 행동을 변화시키는 경우가 많으므로 설득이나 이해가 되지 않는다면 유관자의 행동을 변화시킬 수 없을 뿐 아니라, 프로젝트가 성공적이라고 판단하기 어렵다. 따라서 누군가를 설득하고 이해시키는 작업은 분석가의 중요한 업무중 하나이다.    
    
상대방을 설득하는 데 중요한 부분은 바로 분석가의 태도와 커뮤니케이션 방식이다. 이는 분석가에게 뿐만 아니라 모든 전문가에게 요구되는 기본적인 자질이다. 분석가의 태도는 **기본적으로 데이터를 끈기 있고 집요하게 파고 들며, 분석하고 이해하고 원인을 추론하며 대안을 생각해내는 태도**가 요구된다. 그리고 결과를 누구나 이해하기 쉽게 전달하고 때로는 스토리텔링 등을 통해 설득하고자 하는 노력이 필요하다.

- 경청하고 문제를 이해하고 해결하고자 하는 높은 의지
- 객관적이고 사실에 근거한 결과 도출 (도덕성과 정직성)
- 끊임없이 새로운 것을 학습하고 즐겁게 배우는 태도
- 논리적 사고 및 프로페셔널리즘
- 적극적이고 빠른 피드백/응대
- 명확하고 직관적인 결과/메시지 전달 (두괄식 문장, 간결하게)
- 호기심

### 6. 마치며
이 장에서는 분석 실무에서의 주요 주제/프로세스/팀구성/분석환경/소프트역량에 대해 간략히 살펴보았다. 주요 핵심은 분석가가 개인의 스킬이나 지식에만 몰두하는 것이 아니라 분석가를 둘러싸고 있는 외부 환경과 임무, 협업 방식과 과정, 그리고 이를 보다 윤활하게 해줄 소프트 역량의 중요성을 깨닫는 것이다. 분석가 자체적으로 진행할 수 있는 프로젝트는 거의 없다. 따라서 항상 **겸손/경청하고 새로 배우며 나무 보다는 숲을 넓게 볼 수 있는 분석가**가 되는 것이 중요하다.   
아래의 질문에 간단히 토의하고 이 장을 마치고자 한다.
1. 당신은 왜 분석가가 되려고 하는 것인가? 혹은 왜 분석을 하려고 하는 것인가? 
2. 당신이 데이터를 통해 제공할 수 있는 가치는 무엇일까?
3. 분석가에게 정직성과 신뢰성은 중요한가?
4. 분석 과정에서 시간과 결과 간의 trade-off는 어떻게 다루어야 하는가?
5. 기본적인 분석 방법론 보다 고급 분석 방법론이 더 좋은 것인가?
6. 올바른 질문과 사고를 하려면 어떠한 노력을 해야하는가?
7. 예상하지 못한 결과가 나온다면 어떻게 대처해야하는가?
8. 상대의 이해력이 매우 부족하다면 어떻게 해야하는가?
9. 분석가에게 요구되는 가장 중요한 자질은 무엇인가? 
10. 분석가에게 상상력이 중요한가?