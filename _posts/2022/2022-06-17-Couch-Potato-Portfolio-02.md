---
layout: post
title:  "카우치 포테이토 포트폴리오 02：응용"
description: "카우치 포테이토 포트폴리오, 입맛에 맞게 응용해 보자"
categories: [투자전략]
tags: ["카우치 포테이토", 포트폴리오, 자산배분, 정적자산배분]
---

## 들어가며

가장 기본적이고 단순하지만 상당히 강력한 카우치 포테이토 포트폴리오(couch potato portfolio, CP)에 대해 계속 알아보도록 하자. 

CP에 조금씩 변형을 주면 우리가 알고 있는 유명한 정적자산배분 포트폴리오들이 만들어진다. 이들에 대해서는 향후에 차근차근 알아보도록 하자. 여기에서는 CP의 의미를 벗어나지 않는 한도 내에서 약간의 변형만 해보기로 한다. 

## 응용하기

먼저 주식과 채권의 일부를 다른 자산으로 꾸며보면 어떨까. 데이터 한계로 백테스트 기간이 조금 짧기는 하지만 인상적인 결과가 나타났다.(2011-2022) 약간의 변화를 주었을 뿐이지만 MDD가 크게 하락하지 않으면서 CARG에 유의미한 변화가 있었다. 특히 SPY 40%, TIP 40%, QQQ 10%, SCHD 10% 조합이 눈에 띈다. 

| 전략 │ CARG  | MDD  | 백테스트 |
|:---:|:-----:|:----:|:-----------:|
| SPY+TIP  | 8.40% | -10.02% | [백테스트](https://www.portfoliovisualizer.com/backtest-portfolio?s=y&timePeriod=4&startYear=1985&firstMonth=1&endYear=2022&lastMonth=12&calendarAligned=true&includeYTD=false&initialAmount=10000&annualOperation=0&annualAdjustment=0&inflationAdjusted=true&annualPercentage=0.0&frequency=4&rebalanceType=1&absoluteDeviation=5.0&relativeDeviation=25.0&leverageType=0&leverageRatio=0.0&debtAmount=0&debtInterest=0.0&maintenanceMargin=25.0&leveragedBenchmark=false&reinvestDividends=true&showYield=false&showFactors=false&factorModel=3&benchmark=-1&benchmarkSymbol=SPY&portfolioNames=false&portfolioName1=Portfolio+1&portfolioName2=Portfolio+2&portfolioName3=Portfolio+3&symbol1=SPY&allocation1_1=50&allocation1_2=40&allocation1_3=40&symbol2=TIP&allocation2_1=50&allocation2_2=40&allocation2_3=40&symbol3=QQQ&allocation3_2=10&allocation3_3=10&symbol4=VNQ&allocation4_2=10&symbol5=SCHD&allocation5_3=10&symbol6=GLD) |
| QQQ10+VNQ10  | 9.68% | -11.82% | 상동 |
| QQQ10+SCHD10  | 10.13% | -11.30% | 상동 |
| QQQ10+GLD10  | 8.89% | -9.79% | [백테스트](https://www.portfoliovisualizer.com/backtest-portfolio?s=y&timePeriod=4&startYear=1985&firstMonth=1&endYear=2022&lastMonth=12&calendarAligned=true&includeYTD=false&initialAmount=10000&annualOperation=0&annualAdjustment=0&inflationAdjusted=true&annualPercentage=0.0&frequency=4&rebalanceType=1&absoluteDeviation=5.0&relativeDeviation=25.0&leverageType=0&leverageRatio=0.0&debtAmount=0&debtInterest=0.0&maintenanceMargin=25.0&leveragedBenchmark=false&reinvestDividends=true&showYield=false&showFactors=false&factorModel=3&benchmark=-1&benchmarkSymbol=SPY&portfolioNames=false&portfolioName1=Portfolio+1&portfolioName2=Portfolio+2&portfolioName3=Portfolio+3&symbol1=SPY&allocation1_1=50&allocation1_2=40&allocation1_3=40&symbol2=TIP&allocation2_1=50&allocation2_2=40&allocation2_3=40&symbol3=QQQ&allocation3_2=10&symbol4=VNQ&symbol5=SCHD&allocation5_3=10&symbol6=GLD&allocation6_2=10&allocation6_3=10) |
| SCHD10+GLD10  | 8.40% | -10.06% | 상동 |
| SPY  | 9.47% | -19.43% | 상동 |

## 결론

CP는 매우 단순하지만 자산배분의 기초에 충실하고 성과도 뒤지지 않는 훌륭한 전략이라는 사실을 확인할 수 있었다. 게다가 이를 바탕으로 자신의 입맛에 맞게 조금씩 변형시켜 나간다면 다양한 전략으로 확장시켜 나갈 수 있다.

## REF

* [게으른 퀀트 / 카우치 포터이토](https://lazyquant.xyz/allocation/detail/CP)
* [자산배분전략 S4](https://investstory-k.tistory.com/107)
* [[GAM] '카우치 포테이토 포트폴리오' 게으른 투자자들을 위한 전략](https://www.newspim.com/news/view/20210730000815)

