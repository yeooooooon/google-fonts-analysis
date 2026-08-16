# 🔤 Google Fonts Analysis
> Google Fonts의 메타데이터를 수집하고 정제한 뒤, 웹폰트 트렌드와 기능적 특성을 분석한 데이터 프로젝트입니다.

## 01. 프로젝트 개요
Google Fonts API를 활용해 폰트 메타데이터를 수집하고, 카테고리, 기능, 언어 지원, 인기 순위 등을 분석했습니다.
본 프로젝트는 단순 데이터 정리가 아니라 최근 웹 디자인 트렌드를 반영하는 폰트의 변화 흐름을 살펴보는 데 초점을 두고 있습니다.

## 02. 분석 목적
- 웹폰트 스타일 변화 분석
- Variable Font, weight, italic 등 기능 변화 분석
- 언어 지원 특성 분석
- 인기 폰트의 카테고리 집중도 분석
- 웹 디자인 트렌드 인사이트 도출

## 03. 기능 요약
- **데이터 수집**: Google Fonts API를 통해 웹폰트 메타데이터 수집
- **전처리**: variants, subsets, lastModified, popularity_rank 정리
- **분석**: 카테고리, 기능성, 언어 지원, 인기 폰트 비교
- **시각화**: 기간별 및 구간별 비율 비교 그래프 생성
- **결과 저장**: 정제된 데이터셋을 CSV로 저장

## 04. 기술 스택
- **Language**: Python
- **Notebook**: Jupyter Notebook
- **Data Processing**: pandas, numpy
- **Visualization**: matplotlib, seaborn
- **API & Data Handling**: requests, json
- **Environment**: python-dotenv
- **Version Control**: Git, GitHub

## 05. Notebook 작업 흐름
1. `Google Fonts API`로 원본 메타데이터 수집
2. `DataFrame`으로 구조를 파악하고 결측치 확인
3. `variants`, `subsets`, `axes` 등을 정리해 분석용 컬럼 생성
4. `최근 12개월 vs 이전` 구간을 기준으로 가설 검증
5. `카테고리`, `Variable Font`, `언어 지원`, `인기 순위` 비교 시각화
6. 정제된 결과를 `data/processed/fonts_cleaned.csv`로 저장

## 06. Key Findings
분석 결과, 최근 웹폰트는 `Sans-serif` 비중이 증가하고 있었고, 기능적으로는 `Variable Font`와 다양한 weight 지원이 확산되는 추세를 확인했습니다.
또한 다국어 지원 범위가 넓어지는 흐름 속에서, 실제 웹 UI에서는 가독성과 유연성을 강조하는 폰트 선택이 두드러졌습니다.

## 07. 기대 효과
- 웹폰트 트렌드 이해를 위한 데이터 기반 인사이트 확보
- 폰트 선택 기준을 정량적으로 파악할 수 있는 분석 기반 마련
- UI/UX 설계, 브랜드 폰트 선정, 디지털 콘텐츠 제작에 활용 가능
- 이후 추천 시스템, 대시보드, 시각화 확장 프로젝트로 연결 가능

## 08. 프로젝트 구조
- `google_fonts.ipynb` : 데이터 수집, 전처리, 가설 검증, 시각화 노트북
- `data/raw/google_fonts_raw.json` : 원본 Google Fonts 데이터
- `data/processed/fonts_cleaned.csv` : 정제된 분석 데이터
- `.gitignore` : 민감한 로컬 파일과 원본 데이터 제외 설정