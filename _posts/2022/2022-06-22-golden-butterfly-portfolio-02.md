---
layout: post
title:  "황금나비 포트폴리오 02：응용"
description: "황금나비 포트폴리오를 AOA AOR AOM AOK 시리즈로 구현한다면"
categories: [투자전략]
tags: [황금나비, 포트폴리오, 자산배분, 정적자산배분]
---

## 들어가며

황금나비 포트폴리오를 조금 더 간단히 만들 수는 없을까? 핵심은 주식과 채권 사이에 금과 같이 물가상승을 햇지할 수 있는 자산을 끼워 넣어 균형을 맞추는 것이다. 그렇다면 이미 주식과 채권을 일정 비율로 관리해 주는 AOK, AOM, AOR, AOA를 이용할 수 있지 않을까? 이들 ETF에 대해서는 [이 글](https://strikebell.tistory.com/68)을 참조하자. 백테스트는 데이터 한계로 인해 2011년부터 2019년까지로 설정하였다. 2019년까지로 정한 것은 코로나라는 특수 상황을 배제하기 위함이다. 

## TAKE1: AOA을 이용해 보자. 

AOA은 주식과 채권을 8:2의 비중으로 분산투자하는 공격적인 ETF이다. 따라서 여기에 채권과 금을 조금 섞어 준다면 비슷한 성과를 올릴 수 있지 않을까? 대략 AOA 50%, 채권 30%, 금 20%를 투자하면 주식 40%, 채권 40%, 금 20%에 근접하게 된다. 채권은 장기채에 30%를 넣는 방법(ⓐ)과 단기채에 30%를 넣는 방법(ⓑ) 두 가지로 백테스트를 진행하였다. [백테스트 결과](https://www.portfoliovisualizer.com/backtest-portfolio?s=y&timePeriod=4&startYear=1985&firstMonth=1&endYear=2019&lastMonth=12&calendarAligned=true&includeYTD=false&initialAmount=10000&annualOperation=0&annualAdjustment=0&inflationAdjusted=true&annualPercentage=0.0&frequency=4&rebalanceType=1&absoluteDeviation=5.0&relativeDeviation=25.0&leverageType=0&leverageRatio=0.0&debtAmount=0&debtInterest=0.0&maintenanceMargin=25.0&leveragedBenchmark=false&reinvestDividends=true&showYield=false&showFactors=false&factorModel=3&portfolioNames=false&portfolioName1=Portfolio+1&portfolioName2=Portfolio+2&portfolioName3=Portfolio+3&symbol1=AOA&allocation1_2=50&allocation1_3=50&symbol3=SPY&allocation3_1=20&symbol4=VBR&allocation4_1=20&symbol6=VGLT&allocation6_1=20&allocation6_2=30&allocation6_3=0&symbol7=VGSH&allocation7_1=20&allocation7_2=0&allocation7_3=30&symbol8=SCHD&symbol9=GLD&allocation9_1=20&allocation9_2=20&allocation9_3=20&symbol10=TIP) 장기채 30%를 더하면 오리지날 황금나비 포트폴리오의 성과에 근접하게 나타났다. 다만 MDD는 상대적으로 높게 나타났다. 

| 전략 │ CARG  | MDD  |
|:---:|:-----:|:----:|
| 오리지날  | 6.83%  | -5.71%  |
| ⓐAOA50 & 장기채30  | 6.83%  | -7.49% |
| ⓑAOA50 & 단기채30  | 5.01%  |  -7.65% |

## TAKE2: AOR을 이용해 보자. 

AOR은 주식과 채권을 6:4의 비중으로 분산 투자하는 균형 잡힌 ETF이다. 따라서 금을 조금 섞어 준다면 비슷한 성과를 올릴 수 있지 않을까? 대략 AOR 80%, 금 20%를 투자하면 주식 48%, 채권 32%, 금 20%에 근접하게 된다.(ⓒ) 또 AOR 70%, 장기채 10%, 금 20%에 투자하면 주식 42%, 채권 38%, 금 20%에 근접하게 된다.(ⓓ) [백테스트 결과](https://www.portfoliovisualizer.com/backtest-portfolio?s=y&timePeriod=4&startYear=1985&firstMonth=1&endYear=2019&lastMonth=12&calendarAligned=true&includeYTD=false&initialAmount=10000&annualOperation=0&annualAdjustment=0&inflationAdjusted=true&annualPercentage=0.0&frequency=4&rebalanceType=1&absoluteDeviation=5.0&relativeDeviation=25.0&leverageType=0&leverageRatio=0.0&debtAmount=0&debtInterest=0.0&maintenanceMargin=25.0&leveragedBenchmark=false&reinvestDividends=true&showYield=false&showFactors=false&factorModel=3&portfolioNames=false&portfolioName1=Portfolio+1&portfolioName2=Portfolio+2&portfolioName3=Portfolio+3&symbol1=AOR&allocation1_2=80&allocation1_3=70&symbol3=SPY&allocation3_1=20&symbol4=VBR&allocation4_1=20&symbol6=VGLT&allocation6_1=20&allocation6_3=10&symbol7=VGSH&allocation7_1=20&symbol8=SCHD&symbol9=GLD&allocation9_1=20&allocation9_2=20&allocation9_3=20&symbol10=TIP) 두 가지 모두 오리지날 버전에 비해 CARG가 낮고 MDD가 높게 나타났다. 

| 전략 │ CARG  | MDD  |
|:---:|:-----:|:----:|
| 오리지날  | 6.83%  | -5.71%  |
| ⓒAOR80 | 6.16%  | -7.85% |
| ⓓAOR70 & 장기채10 | 6.15%  | -6.83% |

## TAKE3: AOM을 이용해 보자. 

AOR은 주식과 채권을 4:6의 비중으로 분산 투자하는 균형 잡힌 ETF이다. 따라서 금을 조금 섞어 준다면 비슷한 성과를 올릴 수 있지 않을까? 대략 AOM 80%, 금 20%를 투자하면 주식 32%, 채권 48%, 금 20%에 근접하게 된다.(ⓔ) 이대로는 CARG가 낮게 나타날 것이기에 주식 비중을 조금 더한 버전(ⓕ, ⓖ)도 함께 백테스트 해 보았다. [백테스트 결과](https://www.portfoliovisualizer.com/backtest-portfolio?s=y&timePeriod=4&startYear=2011&firstMonth=1&endYear=2019&lastMonth=12&calendarAligned=true&includeYTD=false&initialAmount=10000&annualOperation=0&annualAdjustment=0&inflationAdjusted=true&annualPercentage=0.0&frequency=4&rebalanceType=1&absoluteDeviation=5.0&relativeDeviation=25.0&leverageType=0&leverageRatio=0.0&debtAmount=0&debtInterest=0.0&maintenanceMargin=25.0&leveragedBenchmark=false&reinvestDividends=true&showYield=false&showFactors=false&factorModel=3&portfolioNames=false&portfolioName1=Portfolio+1&portfolioName2=Portfolio+2&portfolioName3=Portfolio+3&symbol1=AOM&allocation1_1=80&allocation1_2=70&allocation1_3=60&symbol3=SPY&symbol4=VBR&symbol5=QQQ&allocation5_2=10&allocation5_3=20&symbol6=VGLT&symbol7=VGSH&symbol8=SCHD&symbol9=GLD&allocation9_1=20&allocation9_2=20&allocation9_3=20&symbol10=TIP) 예상과 같이 AOM에 금만 더했을 때에는 오리지날 버전보다 CARG가 낮았다. 또 여기에 주식을 더할수록 CARG는 더 높아졌는데, 흥미로운 점은 MDD가 크게 증가하지 않았다는 점이다. 

| 전략 │ CARG  | MDD  |
|:---:|:-----:|:----:|
| 오리지날  | 6.83%  | -5.71%  |
| ⓔAOM80 | 4.83%  | -5.57% |
| ⓕAOM70 & QQQ10 | 6.05%  | -5.72% |
| ⓖAOM60 & QQQ20 | 7.27%  | -5.99% |

## TAKE4: AOK를 이용해 보자. 

AOK는 주식과 채권을 3:7의 비중으로 분산투자하는 보수적인 ETF이다. 따라서 금을 조금 섞어 주고 주식을 추가해 준다면 비슷한 성과를 올릴 수 있지 않을까? 대략 AOK 60%, 금 20%, 주식 20%에 투자하면 주식 38%, 채권 42%, 금 20%에 근접하게 된다.(ⓗ) 이대로는 CARG가 낮게 나타날 것이기에 주식 비중을 조금 더해서(ⓘ, ⓙ)도 함께 백테스트 해 보았다. [백테스트 결과](https://www.portfoliovisualizer.com/backtest-portfolio?s=y&timePeriod=4&startYear=2011&firstMonth=1&endYear=2019&lastMonth=12&calendarAligned=true&includeYTD=false&initialAmount=10000&annualOperation=0&annualAdjustment=0&inflationAdjusted=true&annualPercentage=0.0&frequency=4&rebalanceType=1&absoluteDeviation=5.0&relativeDeviation=25.0&leverageType=0&leverageRatio=0.0&debtAmount=0&debtInterest=0.0&maintenanceMargin=25.0&leveragedBenchmark=false&reinvestDividends=true&showYield=false&showFactors=false&factorModel=3&portfolioNames=false&portfolioName1=Portfolio+1&portfolioName2=Portfolio+2&portfolioName3=Portfolio+3&symbol1=AOK&allocation1_1=60&allocation1_2=50&allocation1_3=40&symbol3=SPY&symbol4=VBR&symbol5=QQQ&allocation5_1=20&allocation5_2=30&allocation5_3=40&symbol6=VGLT&symbol7=VGSH&symbol8=SCHD&symbol9=GLD&allocation9_1=20&allocation9_2=20&allocation9_3=20&symbol10=TIP)

| 전략 │ CARG  | MDD  |
|:---:|:-----:|:----:|
| 오리지날  | 6.83%  | -5.71%  |
| ⓗAOK60 & QQQ20 | 6.80%  | -5.11% |
| ⓘAOK50 & QQQ30 | 8.10%  | -6.37% |
| ⓙAOK40 & QQQ40 | 9.38%  | -7.83% |



## 결론

AOA, AOR, AOM, AOK 어떤 것을 사용해도 비중만 유사하게 조정하면 오리지날 황금나비 버전과 유사한 CARG를 얻을 수 있었다. 하지만 MDD의 경우는 조금 달랐는데, AOA이나 AOR을 이용했을 때 보다 AOM이나 AOK을 이용했을 때 MDD가 더 유리하게 나타났다. 

그렇다면 이들 ETF를 고려하는 것이 어떤 점에서 유리할까. 첫째로 사고 파는 종목 수를 줄일 수 있기 때문에 관리가 편리하다. 오리지날 버전은 5개 이상의 ETF를 관리해야 하지만 AOA 시리즈를 이용하면 3개 ETF 정도만 관리하면 된다. 둘째로 국가간 자산 배분이 가능하다는 점이다. AOA 시리즈는 미국 이외 국가의 주식도 포함되어 있어 국가별 자산 배분의 효과도 누릴 수 있다. 따라서 오리지날 버전을 SPY 등으로 구성했을 때보다 국가 간 자산 배분 효과를 볼 수 있다. 

그렇다면 어떤 버전을 골라야 할까. CARG는 대략 유사하므로 MDD 측면에서 유리한 AOM이나 AOK를 이용하는 편이 유리할 것 같다. 오리지날보다 조금 더 수익을 기대한다면 ⓖAOM60 & QQQ20 전략이 적당할 듯하다. 마지막으로 오리지날 황금나비를 조금 공격적으로 운용하고자 한다면 ⓙAOM40 & QQQ40 전략까지 고려해 볼 수 있을 것 같다. QQQ가 40%나 되지만 MDD가 -10을 넘지 않기 때문이다. [백테스트 결과](https://www.portfoliovisualizer.com/backtest-portfolio?s=y&timePeriod=4&startYear=2011&firstMonth=1&endYear=2019&lastMonth=12&calendarAligned=true&includeYTD=false&initialAmount=10000&annualOperation=0&annualAdjustment=0&inflationAdjusted=true&annualPercentage=0.0&frequency=4&rebalanceType=1&absoluteDeviation=5.0&relativeDeviation=25.0&leverageType=0&leverageRatio=0.0&debtAmount=0&debtInterest=0.0&maintenanceMargin=25.0&leveragedBenchmark=false&reinvestDividends=true&showYield=false&showFactors=false&factorModel=3&portfolioNames=false&portfolioName1=Portfolio+1&portfolioName2=Portfolio+2&portfolioName3=Portfolio+3&symbol1=AOM&allocation1_1=60&symbol2=AOK&allocation2_2=60&allocation2_3=40&symbol3=SPY&symbol4=VBR&symbol5=QQQ&allocation5_1=20&allocation5_2=20&allocation5_3=40&symbol6=VGLT&symbol7=VGSH&symbol8=SCHD&symbol9=GLD&allocation9_1=20&allocation9_2=20&allocation9_3=20&symbol10=TIP)

| 전략 │ CARG  | MDD  |
|:---:|:-----:|:----:|
| 오리지날  | 6.83%  | -5.71%  |
| ⓖAOM60 & QQQ20 | 7.27%  | -5.99% |
| ⓗAOK60 & QQQ20 | 6.80%  | -5.11% |
| ⓙAOK40 & QQQ40 | 9.38%  | -7.83% |