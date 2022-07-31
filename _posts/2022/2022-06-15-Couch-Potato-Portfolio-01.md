---
layout: post
title:  "카우치 포테이토 포트폴리오 01：탐색"
description: "카우치 포테이토 포트폴리오, 자산 배분의 기본"
categories: [투자전략]
tags: ["카우치 포테이토", 포트폴리오, 자산배분, 정적자산배분]
---

## 들어가며

정적 자산 배분 방법으로 영구 포트폴리오, 올시즌 포트폴리오 등이 유명하다. 하지만 가장 기본적인 포트폴리오라고 한다면 "카우치 포테이토 포트폴리오(couch potato portfolio, CP)"를 들 수 있다. 가장 기본적이고 단순하지만 상당히 강력한 카우치 포테이토 포트폴리오에 대해 알아보도록 하자. 

## 의미

미국 영화나 드라마를 보면 소파에 앉아 과자를 먹으며 TV나 영화를 보는 장면이 가끔 등장한다. ["카우치 포테이토"](https://ko.wikipedia.org/wiki/%EC%B9%B4%EC%9A%B0%EC%B9%98_%ED%8F%AC%ED%85%8C%EC%9D%B4%ED%86%A0)는 이런 모습을 묘사한 말로, 만사가 귀찮아 하는 사람을 가리킨다. CP는 이런 귀찮은 사람이라도 할 수 있다, 혹은 이런 귀찮은 사람에게 잘 맞는다는 의미에서 붙여진 이름이다. 

## 방법

CP는 단 2가지 자산으로 구성된 자산 배분 방법이다. 시장 전체 주식을 추종하는 주식과 물가 연동 채권이 그것이다. ETF ticker로 환원하면 VTI와 TIP 정도가 되겠다. 물론 VTI는 SPY 등으로, TIP는 VTIP나 SCHP 등으로 교체해도 좋다. 중요한 점은 주식과 채권을 5:5로 구성한다는 점이다. 특징이라고 한다면 채권 자산을 일반적인 장기채나 단기채가 아닌 물가연동채권으로 적용했다는 점이다. 

물가연동채권은 물가에 따라 이자와 원금이 조정된다. 대표적으로 TIP 등이 이를 추종하는 ETF이다. 국내에서도 최근 물가연동채권을 추종하는 [ETF](https://finance.naver.com/item/main.naver?code=430500)가 상장되었다. 

## 백테스트

CP는 매우 단순한 포트폴리오지만 무시할 수 없는 성과를 보여준다. SPY와 TIP를 백테스트 했을 때(2004-2022) 다음과 같은 성과를 보였다. 방법은 매우 단순하지만 다른 정적자산분배 전략과 비교했을 때 손색이 없는 성과이다. 

| 전략 │ CARG  | MDD  | 백테스트 |
|:---:|:-----:|:----:|:-----------:|
| SPY+TIP  | 7.08% | -27.06% | [백테스트](https://www.portfoliovisualizer.com/backtest-portfolio?s=y&timePeriod=4&startYear=1985&firstMonth=1&endYear=2022&lastMonth=12&calendarAligned=true&includeYTD=false&initialAmount=10000&annualOperation=0&annualAdjustment=0&inflationAdjusted=true&annualPercentage=0.0&frequency=4&rebalanceType=1&absoluteDeviation=5.0&relativeDeviation=25.0&leverageType=0&leverageRatio=0.0&debtAmount=0&debtInterest=0.0&maintenanceMargin=25.0&leveragedBenchmark=false&reinvestDividends=true&showYield=false&showFactors=false&factorModel=3&benchmark=-1&benchmarkSymbol=SPY&portfolioNames=false&portfolioName1=Portfolio+1&portfolioName2=Portfolio+2&portfolioName3=Portfolio+3&symbol1=SPY&allocation1_1=50&symbol2=TIP&allocation2_1=50) |
| SPY  | 9.47% | -50.80% | 상동 |

자산배분의 기본은 주식과 채권이므로 CP의 자산배분 전략은 기본에 매우 충실한 전략이라고 할 수 있다. 덧붙이자면 백테스트 수치 면에서는 TIP 대신 단기채권(SHY)를 적용했을 때는 성과가 좋지 않았고 장기채권(TLT)을 선택했을 때는 더 성과가 좋았다. 장기채권의 경우에는 다른 복잡한 포트폴리오와 비교했을 때 MDD는 조금 컸지만 CARG 측면에서는 뒤지지 않는 수치였다. 

| 전략 │ CARG  | MDD  | 백테스트 |
|:---:|:-----:|:----:|:-----------:|
| SPY+TIP  | 7.08% | -27.06% | [백테스트](https://www.portfoliovisualizer.com/backtest-portfolio?s=y&timePeriod=4&startYear=1985&firstMonth=1&endYear=2022&lastMonth=12&calendarAligned=true&includeYTD=false&initialAmount=10000&annualOperation=0&annualAdjustment=0&inflationAdjusted=true&annualPercentage=0.0&frequency=4&rebalanceType=1&absoluteDeviation=5.0&relativeDeviation=25.0&leverageType=0&leverageRatio=0.0&debtAmount=0&debtInterest=0.0&maintenanceMargin=25.0&leveragedBenchmark=false&reinvestDividends=true&showYield=false&showFactors=false&factorModel=3&benchmark=-1&benchmarkSymbol=SPY&portfolioNames=false&portfolioName1=Portfolio+1&portfolioName2=Portfolio+2&portfolioName3=Portfolio+3&symbol1=SPY&allocation1_1=50&allocation1_2=50&allocation1_3=50&symbol2=TIP&allocation2_1=50&symbol3=TLT&allocation3_2=50&symbol4=SHY&allocation4_3=50) |
| SPY+TLT  | 8.12% | -18.17% | 상동 |
| SPY+SHY  | 5.99% | -24.19% | 상동 |
| SPY  | 9.47% | -50.80% | 상동 |

CP에서 비중을 조금 조정하여 주식 60%, 채권 40%의 조합을 살펴보자. 이는 미국에서 자산 분배의 기준처럼 여겨지는 비율이다. 당연하게도 CARG 측면에서 다소 이점이 있었으나 MDD가 하락하는 결과를 나타냈다. 

| 전략 │ CARG  | MDD  | 백테스트 |
|:---:|:-----:|:----:|:-----------:|
| SPY+TIP  | 7.62% | -32.16% | [백테스트](https://www.portfoliovisualizer.com/backtest-portfolio?s=y&timePeriod=4&startYear=1985&firstMonth=1&endYear=2022&lastMonth=12&calendarAligned=true&includeYTD=false&initialAmount=10000&annualOperation=0&annualAdjustment=0&inflationAdjusted=true&annualPercentage=0.0&frequency=4&rebalanceType=1&absoluteDeviation=5.0&relativeDeviation=25.0&leverageType=0&leverageRatio=0.0&debtAmount=0&debtInterest=0.0&maintenanceMargin=25.0&leveragedBenchmark=false&reinvestDividends=true&showYield=false&showFactors=false&factorModel=3&benchmark=-1&benchmarkSymbol=SPY&portfolioNames=false&portfolioName1=Portfolio+1&portfolioName2=Portfolio+2&portfolioName3=Portfolio+3&symbol1=SPY&allocation1_1=60&allocation1_2=60&allocation1_3=60&symbol2=TIP&allocation2_1=40&symbol3=TLT&allocation3_2=40&symbol4=SHY&allocation4_3=40) |
| SPY+TLT  | 8.55% | -24.64% | 상동 |
| SPY+SHY  | 6.76% | -29.95% | 상동 |
| SPY  | 9.47% | -50.80% | 상동 |

여기까지 살펴보았다면 AOR이 떠오를 것이다. 주식과 채권에 6:4로 투자해 주는 대표적인 자산배분 ETF이다. 데이터 문제로 백테스트 기간이 위와 다르지만, 결과는 아래와 같다. (2008-2022) 흥미롭게도 이 기간에는 장기채권(TLT)보다 물가연동채권(TIP)를 적용했을 때 CARG와 MDD 모두 더 좋았다. AOR은 같은 전략을 취하고 있음에도 결과가 상대적으로 나쁘게 나왔는데, 이는 AOR이 투자하고 있는 주식 비중이 미국, 선진국, 신흥국이 5:4:1의 비중을 가지기 때문인 것 같다. 이 기간에 미국 주식이 다른 선진국과 신흥국보다 더 좋았기 때문이다. 

| 전략 │ CARG  | MDD  | 백테스트 |
|:---:|:-----:|:----:|:-----------:|
| SPY+TIP  | 10.20% | -11.88% | [백테스트](https://www.portfoliovisualizer.com/backtest-portfolio?s=y&timePeriod=4&startYear=1985&firstMonth=1&endYear=2022&lastMonth=12&calendarAligned=true&includeYTD=false&initialAmount=10000&annualOperation=0&annualAdjustment=0&inflationAdjusted=true&annualPercentage=0.0&frequency=4&rebalanceType=1&absoluteDeviation=5.0&relativeDeviation=25.0&leverageType=0&leverageRatio=0.0&debtAmount=0&debtInterest=0.0&maintenanceMargin=25.0&leveragedBenchmark=false&reinvestDividends=true&showYield=false&showFactors=false&factorModel=3&benchmark=-1&benchmarkSymbol=AOR&portfolioNames=false&portfolioName1=Portfolio+1&portfolioName2=Portfolio+2&portfolioName3=Portfolio+3&symbol1=SPY&allocation1_1=60&allocation1_2=60&allocation1_3=60&symbol2=TIP&allocation2_1=40&symbol3=TLT&allocation3_2=40&symbol4=SHY&allocation4_3=40) |
| SPY+TLT  | 10.01%  | -16.61% | 상동 |
| SPY+SHY  | 9.01%  | -11.08% | 상동 |
| AOR  | 7.90% | -13.50% | 상동 |


## REF

* [게으른 퀀트 / 카우치 포터이토](https://lazyquant.xyz/allocation/detail/CP)
* [자산배분전략 S4](https://investstory-k.tistory.com/107)
* [[GAM] '카우치 포테이토 포트폴리오' 게으른 투자자들을 위한 전략](https://www.newspim.com/news/view/20210730000815)
