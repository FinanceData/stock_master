# KRX stock listing data set
KRX(Korea Exchange) stock listing data set (As of September 30, 2018)
* listing stock code and name of KRX
* Includes unlisted stocks 
* includes industry classification and industry name data of DART


# 종목 마스터 데이터셋

종목 마스터 데이터셋은 전체 종목 전체에 대한 산업구분 데이터이다. 상장폐지 종목을 포함하고 있으며, 전자공시(DART)의 산업분류와 산업이름 데이터를 포함하고 있다. (2018.09.30 기준)

#### 주요 사용처
* 주로 종목에 대한 분류, 섹터 분석, 시가총액 분석 등을 위한 용도로 사용할 수 있다.

#### 컬럼
* Symbol: 종목코드
* Name: 종목명
* Market: 'KOSPI', 'KODAQ', 'KONEX'
* Listing: 상장여부 (False 상장폐지 종목)
* Industry: 거래소 산업구분
* Sector: 거래소 산업구분
* Industy_code: 전자공시(DART)의 산업분류 코드
* Industy_name: 전자공시(DART)의 산업 이름

#### 참고사항
* 상장폐지 종목(Listing=False)의 경우 Industry, Sector 정보가 없다
* 전자공시(DART)에 해당 회사의 정보가 없는 경우 Industy_code, Industy_name 정보가 없다

# Dataset
https://github.com/FinanceData/stock_master/raw/master/stock_master.csv.gz 

* CSV (plain text)
* 3,516 rows
* 8 columns

# Usage

```python
import pandas as pd

url = 'https://github.com/FinanceData/stock_master/raw/master/stock_master.csv.gz'
df_master = pd.read_csv(url, dtype={'Symbol':str, 'Industy_code':str} )
df_master.head(10)
```

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Symbol</th>
      <th>Name</th>
      <th>Market</th>
      <th>Listing</th>
      <th>Industry</th>
      <th>Sector</th>
      <th>Industy_code</th>
      <th>Industy_name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>001040</td>
      <td>CJ</td>
      <td>KOSPI</td>
      <td>True</td>
      <td>지주회사</td>
      <td>기타 금융업</td>
      <td>64992</td>
      <td>지주회사</td>
    </tr>
    <tr>
      <th>1</th>
      <td>011150</td>
      <td>CJ씨푸드</td>
      <td>KOSPI</td>
      <td>True</td>
      <td>수산물(어묵,맛살)가공품 도매,원양수산업,수출입</td>
      <td>기타 식품 제조업</td>
      <td>10799</td>
      <td>그 외 기타 식료품 제조업</td>
    </tr>
    <tr>
      <th>2</th>
      <td>012630</td>
      <td>HDC</td>
      <td>KOSPI</td>
      <td>True</td>
      <td>토목공사,건축공사,아파트분양사업,재개발/재건축사업</td>
      <td>건물 건설업</td>
      <td>4111</td>
      <td>주거용 건물 건설업</td>
    </tr>
    <tr>
      <th>3</th>
      <td>082740</td>
      <td>HSD엔진</td>
      <td>KOSPI</td>
      <td>True</td>
      <td>대형선박용엔진,내연발전엔진</td>
      <td>일반 목적용 기계 제조업</td>
      <td>29111</td>
      <td>내연기관 제조업</td>
    </tr>
    <tr>
      <th>4</th>
      <td>001390</td>
      <td>KG케미칼</td>
      <td>KOSPI</td>
      <td>True</td>
      <td>콘크리트혼화제, 비료, 친환경농자재, 수처리제</td>
      <td>기초 화학물질 제조업</td>
      <td>201</td>
      <td>기초 화학물질 제조업</td>
    </tr>
    <tr>
      <th>5</th>
      <td>010060</td>
      <td>OCI</td>
      <td>KOSPI</td>
      <td>True</td>
      <td>타르제품,카본블랙,무수프탈산,농약원제,석탄화학제품,정밀화학제품,플라스틱창호재 제조,판매</td>
      <td>기초 화학물질 제조업</td>
      <td>20129</td>
      <td>기타 기초 무기화학 물질 제조업</td>
    </tr>
    <tr>
      <th>6</th>
      <td>002360</td>
      <td>SH에너지화학</td>
      <td>KOSPI</td>
      <td>True</td>
      <td>합성수지(PS/EPS,ABS수지) 제조</td>
      <td>기초 화학물질 제조업</td>
      <td>201</td>
      <td>기초 화학물질 제조업</td>
    </tr>
    <tr>
      <th>7</th>
      <td>001740</td>
      <td>SK네트웍스</td>
      <td>KOSPI</td>
      <td>True</td>
      <td>종합무역업(전자전기제품,섬유,에너지화학제품,철강금속제품),의류,수입산합판,MDF판매...</td>
      <td>기타 전문 도매업</td>
      <td>467</td>
      <td>기타 전문 도매업</td>
    </tr>
    <tr>
      <th>8</th>
      <td>011810</td>
      <td>STX</td>
      <td>KOSPI</td>
      <td>True</td>
      <td>에너지 원료(석탄,석유),산업기자재(기계부품) 도매</td>
      <td>상품 종합 도매업</td>
      <td>46800</td>
      <td>상품 종합 도매업</td>
    </tr>
    <tr>
      <th>9</th>
      <td>071970</td>
      <td>STX중공업</td>
      <td>KOSPI</td>
      <td>True</td>
      <td>조선기자재, 기계부품, 엔진산업환경발전설비, 플랜트(EPC)</td>
      <td>일반 목적용 기계 제조업</td>
      <td>29119</td>
      <td>기타 기관 및 터빈 제조업</td>
    </tr>
  </tbody>
</table>


```python
len(df_master)
```
```
3516
```
