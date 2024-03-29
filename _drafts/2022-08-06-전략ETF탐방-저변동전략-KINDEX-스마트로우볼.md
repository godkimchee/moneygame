---
layout: post
title:  "전략ETF탐방 × 저변동전략 │ KINDEX 스마트로우볼"
description: ""
categories: ['전략ETF탐방']
tags: [ETF, 퀀트, 저변동전략]
meta:
  ticker: ['322130']
---

## 오늘의 퀀트 전략 ETF

{% include _proj/stETF.md tickers=page.meta.ticker %}

번동성이 낮은 종목으로 포트폴리오를 구성하는 저변동성 전략을 채택한 퀀트 전략 ETF이다. 

## 현황

ETF 현황. 상장(2019년 4월 16일) 이후 현재(2022년 8월 1일)까지 17.78%의 수익률을 나타냈다. 

지수 현황. 최근 3년 동안을 보면, 큰 차이는 아니지만 코스피200 대비 성과가 다소 낮았던 것을 볼 수 있다. 

{% include image.md file="etf-322130-001.png" label="지수 그래프" %}

※ 최근 3년 지수 그래프. ( FnGuide 지수 홈페이지에서 인용 )

포함 종목 Top10은 아래와 같다(2022.08.01 현재). 

|  Symbol |    Constituent   |     Sector     | Weight(%) | 최근 1년 수익률(%) |
|:-------:|:----------------:|:--------------:|:---------:|:------------------:|
| A005930 | 삼성전자         | 하드웨어       |     25.06 |             -22.19 |
| A000660 | SK하이닉스       | 반도체         |      5.12 |             -16.81 |
| A035420 | NAVER            | 소프트웨어     |      4.36 |             -40.25 |
| A005380 | 현대차           | 자동차 및 부품 |      3.54 |             -10.68 |
| A000270 | 기아             | 자동차 및 부품 |      2.75 |              -4.13 |
| A006400 | 삼성SDI          | 하드웨어       |      2.59 |             -23.43 |
| A051910 | LG화학           | 소재           |      2.43 |             -29.40 |
| A207940 | 삼성바이오로직스 | 제약 및 바이오 |      2.25 |              -4.02 |
| A105560 | KB금융           | 은행           |      2.13 |              -6.68 |
| A035720 | 카카오           | 소프트웨어     |      2.10 |             -50.82 |


## 전략 분석

유니버스 구성
* 한국거래소 유가증권시장 상장 종목 중 상장일 1년 이상
* 유니버스 내 거래대금 하위 10% 종목 제외, 최근 3개년 연속 적자 기업 제외

지수 산출
* 변동성지표: 아래 4가지 값의 평균
  - 60일 일간 변동성: 최근 60일 일간 수익률 표준편차의 [z-score](https://ko.wikipedia.org/wiki/%ED%91%9C%EC%A4%80_%EC%A0%90%EC%88%98)
  - 1년 일간 변동성: 최근 1년 일간 수익률 표준편차의 z-score
  - 3년 일간 변동성: 최근 3년 일간 수익률 표준편차의 z-score
  - 3년 주간 변동성: 최근 3년 주간 수익률 표준편차의 z-score

종목 선정
* 변동성지표 하위 45개 종목 이상 편입

편입 비중
* 포트폴리오의 최종 스코어를 최대로 하는 Global Minimum Variance 최적화 기법을 통해 도출된 종목별 비중 사용 ( 최적화 목적은 알겠으나 구체적인 방법은 이해하지 못하였음 )

※ 위 내용은 지수 개발사에서 제공하는 문서의 내용을 바탕으로 하였으나 요약되어 있으므로 본래 방법과 다소 차이가 있을 수 있다.

## 정리

일반적인 저변동 전략과 다른 점은 여러 변동성 수치를 구한 뒤 z-score를 사용하여 표준화 시켰다는 점과, 포트폴리오 편입 비중을 최적화 기법을 통해 도출했다는 점이다. 다만 상장(2019년) 이래로 상승장이 지속되었기 때문에 하락장에서의 성과를 확인할 수 없다. 또한 현재 대형주 중심으로 편입되어 있어 코스피200과 상관성이 높을 것으로 보인다. 
