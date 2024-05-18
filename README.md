## 2022 체육 종합 데이터 분석 및 활용 경진대회

### 활용 언어 및 패키지
<p align="left">
  <a href="https://www.python.org/" target="_blank" rel="noreferrer"> 
    <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="python"/> 
  </a>
  <a href="https://numpy.org/" target="_blank" rel="noreferrer"> 
    <img src="https://img.shields.io/badge/Numpy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="numpy"/> 
  </a>
  <a href="https://matplotlib.org/" target="_blank" rel="noreferrer"> 
    <img src="https://img.shields.io/badge/Matplotlib-ffffff?style=for-the-badge&logo=matplotlib&logoColor=black" alt="matplotlib"/> 
  </a>
  <a href="https://streamlit.io/" target="_blank" rel="noreferrer"> 
    <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="streamlit"/> 
  </a>
  <a href="https://pickle.readthedocs.io/en/stable/" target="_blank" rel="noreferrer"> 
    <img src="https://img.shields.io/badge/Pickle-4CAF50?style=for-the-badge&logo=pickle&logoColor=white" alt="pickle"/> 
  </a>
</p>

### 조 구성원
| 역할 | 이름 |
| ---- | ---- |
| 조장 | 이승렬 |
| 조원 | 박다혜, 조민선 |

### 조 이름
- SKUDAA (SKU DATA ANALYSIS ASSOCIATION)

### 프로젝트 개요
#### 프로젝트 명
장애유형에 따른 장애인 체육 관련시설, 프로그램 소개 및 장애 유형에 따른 운동 추천

#### 프로젝트 주제
지역별 장애인 활용 가능 체육시설 안내 및 세부 신체 조건에 따른 장애인 운동 추천

#### 주제 선정 배경
1. 장애인의 건강과 체력관리를 위한 운동 참여 목적 증가
2. 장애유형을 고려한 생활체육 저변 확대 필요성 강조
3. 장애 유형별 특수성으로 인하여 자생적 활성화에 어려움

이에 따라 체력관리를 위한 장애인 운동 활성화에 필요한 네트워크 구축 및 교류, 장애인 생활체육인 지원과 종목 개발 및 보급 등 사업을 추진

### 프로젝트 요약
- **항목 기입에 따른 시설 출력:** 체육시설과 편의시설 및 장애유형에 따른 활동 가능한 장애인 스포츠 클럽 안내 서비스 구현
- **항목 기입에 따른 운동 추천:** 장애인 신체조건에 따른 체력 측정 이전 나이, 성별, 장애유형, 특이사항 등에 따른 필요 운동 추천 서비스 구현

### 활용 데이터 셋
| Dataset | 설명 | 출처 |
| ------- | ---- | ---- |
| Dataset1 | 장애인 생활체육교실 데이터 | [문화 빅데이터 - 포털](https://www.bigdata-culture.kr) |
| Dataset2 | 장애인 생활체육 동호인 클럽 조회 | [문화 빅데이터 - 포털](https://www.bigdata-culture.kr) |
| Dataset3 | 장애인 스포츠강좌 이용권 시설 인근 편의시설 정보 | [문화 빅데이터 - 포털](https://www.bigdata-culture.kr) |
| Dataset4 | 장애인 체력측정별 추천 운동 데이터 | [문화 빅데이터 - 포털](https://www.bigdata-culture.kr) |

### 데이터 전처리
1. **항목 기입에 따른 시설 출력:** 
   - 전체적인 데이터셋 확인 후 지역 유니크 값 확인
   - 데이터 셋 별 함수 작성
2. **항목 기입에 따른 운동 추천**
   - 컬럼 결측 치 확인 후 일괄적으로 처리
   - 문자열에 따른 코사인 유사도 계산 함수 작성
   - 문자열에 따른 코사인 유사도 계산을 위한 input 데이터 생성
   - 입력 값에 따른 인덱스 값 추출을 위해 인덱스와 컬럼 값 치환

### 기능 구현
- **항목 기입에 따른 운동 추천 - 코사인 유사도를 활용한 추천 시스템 구현**
  - 답변 값에 따라 천체 데이터 기준에 해당되는 인덱스 값 할당 받기
  - 인덱스에 따른 코사인 유사도 값 확인 및 이중 코사인 유사도 범위가 0.75이상 1.0이하인 값에 대해서만 값을 추출
  - 범위 내에 있는 정보 추출 및 추천목록의 정보 추출
  - 기준 데이터셋에서 인덱스 정보에 맞는 운동 결과 추출
