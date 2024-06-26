# 빅데이터를 통한 구미시 상징 조형물 건설

> 구미시 관련 인터넷 뉴스 기사 빅데이터 분석을 통한 구미시 인식 조사 프로젝트

## 📝 프로젝트 개요

- 구미시 상징 조형물 건설을 위해 구미시 관련 인터넷 뉴스 기사 19,324건을 수집하고 분석하여 구미시에 대한 일반인들의 인식을 간접적으로 파악하고자 하는 프로젝트입니다.

- 일반인들이 가장 많이 접하는 매체인 인터넷 뉴스 기사의 특성상, 이를 통해 구미시에 대한 인식을 추측해볼 수 있습니다. 블로그, 트위터 등 일반인들이 직접 작성한 글을 분석하는 것이 더 효과적이나, 관련 데이터가 부족하여 인터넷 뉴스 기사를 분석 대상으로 선정하였습니다.

- **수행 기간**: 2022년 11월
- **분석 대상**: 2018년 1월 1일 ~ 2022년 11월 20일 사이에 보도된 구미시 관련 인터넷 뉴스 기사 19,324건
- **분석 방법**: 
  - 데이터 수집: 빅카인즈 서비스 활용
  - 텍스트 전처리: 한글 문장/단어 추출, 토큰화, 불용어 제거 등
  - 토픽 모델링: BERTopic 활용, 50개 토픽 추출 후 17개 토픽 클러스터로 해석
  - 감정 분석: KLUE-BERT 모델 활용, 중립/긍정/부정으로 분류

## 🛠️ 분석 도구 및 라이브러리
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=Python&logoColor=white"> <img src="https://img.shields.io/badge/BERTopic-000000?style=for-the-badge&logo=BERTopic&logoColor=white"> <img src="https://img.shields.io/badge/KLUE BERT-6DB33F?style=for-the-badge&logo=KLUE BERT&logoColor=white"> 
<img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=Pandas&logoColor=white"> <img src="https://img.shields.io/badge/KoNLPy-3776AB?style=for-the-badge&logo=KoNLPy&logoColor=white">

## 📊 분석 과정 및 결과

### 데이터 수집 및 전처리
- 빅카인즈 서비스를 활용하여 2018년 1월 1일부터 2022년 11월 20일까지 보도된 구미시 관련 인터넷 뉴스 기사 19,324건 수집
- 한글 문장/단어 추출, 토큰화, 불용어 제거 등의 텍스트 전처리 과정 수행
<img width="524" alt="image" src="https://github.com/ANGHOOO/Gumi-Symbolic-Artifact/assets/103275370/4c0719bd-51b2-4180-8f09-cc8797d101ea">


### 기초 통계량 분석
- 월 평균 327건의 구미시 관련 뉴스 기사 보도
- 분야별로는 지역, 경제, 사회, 정치 분야 뉴스가 많은 비중 차지
- 전체 뉴스 기사 워드 클라우드 분석 결과, 산업 클러스터 관련 키워드가 다수 등장
<img width="847" alt="image" src="https://github.com/ANGHOOO/Gumi-Symbolic-Artifact/assets/103275370/475cdf95-0545-4d1f-adc9-10ba2668adca">


### 토픽 모델링
- BERTopic을 활용하여 50개의 토픽 도출 후 유사 토픽 클러스터링 수행
- 총 17개의 토픽 클러스터로 해석
  - 지역산업 및 정치(6,140건; 73%) : 산업 투자, 일자리, 도시 간 관계, 선거 등
  - 사건/사고(2,284건; 27%) : 여아 살인, 경찰 폭행, 농협 선거법 위반, 코로나 확진, 소방 화재 진화 등
<img width="874" alt="image" src="https://github.com/ANGHOOO/Gumi-Symbolic-Artifact/assets/103275370/6b75423f-00e1-48f5-ba2d-4994b368986d">

### 감정 분석  
- KLUE-BERT 모델을 활용하여 뉴스 기사를 중립/긍정/부정으로 분류
- 분류 결과: 중립 10,408건, 긍정 5,219건, 부정 3,697건
- 긍정 비율이 높은 토픽 클러스터
  - 항공 및 도로 사업, 아동 및 지역 기부, 반도체/방산/화학 산업 투자 등
  - 산업 육성 및 투자 관련 긍정 보도가 많음
- 부정 비율이 높은 토픽 클러스터  
  - 대구 낙동강 취수 갈등, 여아 살인 사건, 남아 자살 사건 등
  - 타 도시와의 갈등, 치안 관련 부정 보도가 많음
 
<img width="848" alt="image" src="https://github.com/ANGHOOO/Gumi-Symbolic-Artifact/assets/103275370/ba413374-2973-42a6-8482-09405490cf07">


## 📜 Conclusion

- 구미시 관련 뉴스 기사 빅데이터 분석을 통해 구미시에 대한 일반인들의 인식을 간접적으로 파악
- 지역산업 및 정치 관련 토픽이 전체의 73%로 대다수를 차지하며, 특히 산업 투자 및 기업 육성 관련 긍정 보도가 많음
  - 역동적인 산업도시, 투자가 필요한 도시, 대기업과 상생하는 도시 등의 이미지 형성에 기여할 것으로 추측
- 반면 살인/자살 사건, 대구시와의 갈등 관련 토픽은 부정 보도 비율이 높음  
  - 치안이 좋지 않은 도시, 주변 도시와 갈등이 많은 도시 등의 부정적 인식 형성 가능성 존재
- 본 분석은 인터넷 뉴스 기사만을 대상으로 했다는 한계점 존재
  - 보다 정확한 인식 조사를 위해서는 일반인들이 직접 작성한 데이터 추가 수집 및 분석 필요

## 🔮 추후 분석 방향

- 블로그, 트위터 등 일반인들이 직접 작성한 구미시 관련 데이터 수집 및 분석  
- 구미시 주요 정책, 이벤트 전후 시점 데이터 비교 분석을 통한 정책 효과 파악
- 타 도시 관련 뉴스와의 비교 분석을 통한 구미시만의 특징적 토픽 및 이슈 도출

## 📁 프로젝트 자료

- [분석 보고서](https://drive.google.com/file/d/1uo9oSKBJsRnfH89Qmx7kf7bf4vULUh_2/view?usp=sharing)
