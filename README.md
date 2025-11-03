# 🌍 기대 수명 예측 프로젝트

WHO(세계보건기구)의 데이터를 기반으로 여러 보건 및 경제 지표가 국가의 기대 수명에 어떤 영향을 미치는지 분석하고, 기대 수명을 예측하는 머신러닝 모델을 실습합니다.

## 📂 데이터셋

  - `life_expectancy.csv`: 국가별 연도별 보건, 경제 지표 및 기대 수명 데이터
  - **GitHub Repository**: `https://github.com/thiskorea81/life_expectancy.git`
  - **데이터 출처**: WHO (World Health Organization)

## 📊 속성 정보 (Attribute Information)

| 속성명 (영문) | 속성명 (한글) | 설명 |
| :--- | :--- | :--- |
| `Country` | **국가** | 국가 이름 |
| `Year` | **연도** | 데이터 수집 연도 |
| `Status` | **국가\_상태** | `Developed`(선진국) 또는 `Developing`(개발도상국) |
| `Life expectancy` | **기대\_수명** | 해당 연도 해당 국가의 기대 수명 (세). **(예측 대상)** |
| `Adult Mortality` | **성인\_사망률** | 15세에서 60세 사이 1,000명당 사망자 수 |
| `infant deaths` | **영아\_사망자\_수** | 1,000명 출생아 당 1세 미만 영아 사망자 수 |
| `Alcohol` | **알코올\_소비량** | 15세 이상 인구의 1인당 순수 알코올 소비량 (리터) |
| `percentage expenditure` | **의료비\_지출\_비율** | 1인당 GDP 대비 의료비 지출 비율 (%) |
| `Hepatitis B` | **B형\_간염\_예방접종률** | 1세 아동의 B형 간염 예방접종(HepB) 보급률 (%) |
| `Measles` | **홍역\_발병\_수** | 1,000명당 홍역 발병 건수 |
| `BMI` | **평균\_체질량지수** | 인구의 평균 체질량지수 (BMI) |
| `under-five deaths` | **5세\_미만\_사망자\_수** | 1,000명 출생아 당 5세 미만 사망자 수 |
| `Polio` | **소아마비\_예방접종률** | 1세 아동의 소아마비 예방접종(Pol3) 보급률 (%) |
| `Total expenditure` | **총\_의료비\_지출** | 정부 총 지출 대비 의료비 지출 비율 (%) |
| `Diphtheria` | **디프테리아\_예방접종률**| 1세 아동의 디프테리아 예방접종(Dpt3) 보급률 (%) |
| `HIV/AIDS` | **HIV/AIDS\_사망률** | 1,000명 출생아 당 HIV/AIDS로 인한 5세 미만 사망자 수 |
| `GDP` | **1인당\_GDP** | 1인당 국내총생산 (달러) |
| `Population` | **인구** | 해당 국가의 인구 수 |
| `thinness 1-19 years` | **청소년\_저체중\_비율** | 10-19세 청소년의 저체중 비율 (%) |
| `thinness 5-9 years` | **아동\_저체중\_비율** | 5-9세 아동의 저체중 비율 (%) |
| `Income composition of resources` | **소득\_구성\_지수** | 0에서 1 사이의 인간 개발 지수(HDI) 소득 구성 요소 |
| `Schooling` | **평균\_교육\_기간** | 인구의 평균 교육 기간 (년) |

## 🚀 구글 코랩(Google Colab)에서 실행하기

구글 코랩 환경에서 아래 코드를 순서대로 실행하여 데이터를 간편하게 불러올 수 있습니다.

### 1\. GitHub 저장소 복제

`!git clone` 명령어를 사용하여 GitHub에 있는 데이터 파일을 코랩 환경으로 가져옵니다.

```python
!git clone https://github.com/thiskorea81/life_expectancy.git
```

### 2\. Pandas로 데이터 불러오기

저장소 복제가 완료되면, `pandas` 라이브러리를 사용하여 `life_expectancy.csv` 파일을 DataFrame으로 불러옵니다.

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

# 복제된 폴더 안의 파일 경로를 지정합니다.
# (저장소에 있는 실제 파일명으로 수정해야 할 수 있습니다.)
file_path = '/content/life_expectancy/Life Expectancy Data.csv'

# CSV 파일을 DataFrame으로 읽어옵니다.
df = pd.read_csv(file_path)

# 데이터의 첫 5행을 출력하여 잘 불러왔는지 확인합니다.
df.head()
```
