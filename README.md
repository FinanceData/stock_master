# KRX stock listing data set
KRX(Korea Exchange) stock listing data set (As of September 30, 2018)
* listing stock code and name of KRX
* Includes unlisted stocks 
* includes industry classification and industry name data of DART


# 종목 마스터 데이터셋

종목 마스터 데이터셋은 전체 종목 전체에 대한 산업구분 데이터이다. 비상장 종목을 포함하고 있으며,  전자공시(DART)의 산업분류와 산업이름 데이터를 포함하고 있다. (2018.09.30 기준)

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
