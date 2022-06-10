---
layout: post
title:  "황금나비 포트폴리오 01：탐색"
description: "황금나비 포트폴리오, 어떻게 시작할까?"
categories: [투자전략]
tags: [황금나비, 포트폴리오, 자산배분, 정적자산배분]
---

## 들어가며

정적 자산 배분 방법 가운데, 대표적으로 영구 포트폴리오, 올시즌 포트폴리오 등이 있다. 하지만 내가 생각한 [투자 전략의 기본 원칙]()에 따라 황금나비 포트폴리오가 가장 직관적으로 와 닿아서 이를 선택하였다. 

## 어떤 종목을 선택할 것인가. 

기본적으로 포트폴리오는 "자신의 종류"가 정해져 있을 뿐이다. 따라서 해당 자산을 구체적으로 어떤 종목으로 구성할지에 대해서는 투자자의 재량에 달려 있다. 황금나비 역시 아래와 같이 자산의 종류가 정해져 있을 뿐이다. 

* 20% 전체 주식
* 20% 소형 가치주
* 20% 장기 채권
* 20% 단기 채권
* 20% 금

그렇다면 각각의 자산은 구체적으로 어떤 종목으로 해야 할까. 대표적인 ETF를 활용한다면 다음과 같이 할 수 있을 것이다.(ⓐ)

* 20% 미국 전체 주식 : SPY
* 20% 미국 소형 가치 : VBR
* 20% 장기 채권 : TLT
* 20% 단기 채권 : SHY
* 20% 금 : GLD

물론 SPY는 VOO, TLT는 VGLT, SHY는 VGSH 등으로 바꾸어도 대세에 지장은 없다(수수료가 싸다). 백테스트 결과는 [이와 같다](https://www.portfoliovisualizer.com/backtest-portfolio?s=y&timePeriod=4&startYear=2010&firstMonth=1&endYear=2019&lastMonth=12&calendarAligned=true&includeYTD=false&initialAmount=10000&annualOperation=0&annualAdjustment=0&inflationAdjusted=true&annualPercentage=0.0&frequency=4&rebalanceType=1&absoluteDeviation=5.0&relativeDeviation=25.0&leverageType=0&leverageRatio=0.0&debtAmount=0&debtInterest=0.0&maintenanceMargin=25.0&leveragedBenchmark=false&reinvestDividends=true&showYield=false&showFactors=false&factorModel=3&benchmark=-1&benchmarkSymbol=SPY&portfolioNames=false&portfolioName1=Portfolio+1&portfolioName2=Portfolio+2&portfolioName3=Portfolio+3&symbol1=SPY&allocation1_1=20&allocation1_2=20&symbol2=VBR&allocation2_1=20&allocation2_2=20&symbol4=TLT&allocation4_1=20&symbol5=SHY&allocation5_1=20&symbol6=VGLT&allocation6_2=20&symbol7=VGSH&allocation7_2=20&symbol8=GLD&allocation8_1=20&allocation8_2=20).

## 좀더 공격적이 되어 볼까

MDD는 충분히 만족스럽지만 CAGR이 6.95%로 조금 불만스럽다. 조금 더 공격적으로 바꾸어보면 어떨까. 황금나비에서 수익을 노린 부분은 "소형 가치주" 부분이다. 이를 조금 다른 관점에서 "기술 성장주" 즉 QQQ로 바꾸어 보면 어떨까.(ⓑ) [백테스트 결과](https://www.portfoliovisualizer.com/backtest-portfolio?s=y&timePeriod=4&startYear=2010&firstMonth=1&endYear=2019&lastMonth=12&calendarAligned=true&includeYTD=false&initialAmount=10000&annualOperation=0&annualAdjustment=0&inflationAdjusted=true&annualPercentage=0.0&frequency=4&rebalanceType=1&absoluteDeviation=5.0&relativeDeviation=25.0&leverageType=0&leverageRatio=0.0&debtAmount=0&debtInterest=0.0&maintenanceMargin=25.0&leveragedBenchmark=false&reinvestDividends=true&showYield=false&showFactors=false&factorModel=3&benchmark=-1&benchmarkSymbol=SPY&portfolioNames=false&portfolioName1=Portfolio+1&portfolioName2=Portfolio+2&portfolioName3=Portfolio+3&symbol1=SPY&allocation1_1=20&allocation1_2=20&symbol2=VBR&allocation2_1=20&symbol3=QQQ&allocation3_2=20&symbol6=VGLT&allocation6_1=20&allocation6_2=20&symbol7=VGSH&allocation7_1=20&allocation7_2=20&symbol9=GLD&allocation9_1=20&allocation9_2=20). MDD도 약간 줄었지만 무엇보다 CAGR이 8.20%로 늘어났다. ( 물론 과적합 문제일 수도 있지만 .... )

| 전략 | CARG  | MDD  |
|:---:|:-----:|:----:|
| ⓐ  | 6.85% | -5.71% |
| ⓑ  | 8.20% | -5.23% |

## 황금나비의 몸통을 바꿔볼까

황금나비의 몸통은 주식도 채권도 아닌 금으로 되어 있다. 인플레이션을 햇지하기 위한 목적이다. 목적이 유사한 자산을 섞어보면 어떨까. ⓒ원자재(DBC), ⓓ물가 연동 채권(TIP), ⓔ고배당주(SCHD), ⓕ리츠(VNQ) 등을 생각해 보았다. 

ⓒ와 ⓓ의 [백테스트 결과](https://www.portfoliovisualizer.com/backtest-portfolio?s=y&timePeriod=4&startYear=2010&firstMonth=1&endYear=2019&lastMonth=12&calendarAligned=true&includeYTD=false&initialAmount=10000&annualOperation=0&annualAdjustment=0&inflationAdjusted=true&annualPercentage=0.0&frequency=4&rebalanceType=1&absoluteDeviation=5.0&relativeDeviation=25.0&leverageType=0&leverageRatio=0.0&debtAmount=0&debtInterest=0.0&maintenanceMargin=25.0&leveragedBenchmark=false&reinvestDividends=true&showYield=false&showFactors=false&factorModel=3&benchmark=-1&benchmarkSymbol=SPY&portfolioNames=false&portfolioName1=Portfolio+1&portfolioName2=Portfolio+2&portfolioName3=Portfolio+3&symbol1=SPY&allocation1_1=20&allocation1_2=20&allocation1_3=20&symbol2=VBR&symbol3=QQQ&allocation3_1=20&allocation3_2=20&allocation3_3=20&symbol6=VGLT&allocation6_1=20&allocation6_2=20&allocation6_3=20&symbol7=VGSH&allocation7_1=20&allocation7_2=20&allocation7_3=20&symbol8=GLD&allocation8_1=20&allocation8_2=10&allocation8_3=10&symbol9=DBC&allocation9_2=10&symbol10=TIP&allocation10_3=10)

| 전략 | CARG  | MDD  |
|:---:|:-----:|:----:|
| ⓑ  | 8.20% | -5.23% |
| ⓒ  | 7.64% | -7.02% |
| ⓓ  | 8.40% | -5.64% |

ⓔ와 ⓕ를 넣은 [백테스트 결과](https://www.portfoliovisualizer.com/backtest-portfolio?s=y&timePeriod=4&startYear=2010&firstMonth=1&endYear=2019&lastMonth=12&calendarAligned=true&includeYTD=false&initialAmount=10000&annualOperation=0&annualAdjustment=0&inflationAdjusted=true&annualPercentage=0.0&frequency=4&rebalanceType=1&absoluteDeviation=5.0&relativeDeviation=25.0&leverageType=0&leverageRatio=0.0&debtAmount=0&debtInterest=0.0&maintenanceMargin=25.0&leveragedBenchmark=false&reinvestDividends=true&showYield=false&showFactors=false&factorModel=3&benchmark=-1&benchmarkSymbol=SPY&portfolioNames=false&portfolioName1=Portfolio+1&portfolioName2=Portfolio+2&portfolioName3=Portfolio+3&symbol1=SPY&allocation1_1=20&allocation1_2=20&allocation1_3=20&symbol2=VBR&symbol3=QQQ&allocation3_1=20&allocation3_2=20&allocation3_3=20&symbol6=VGLT&allocation6_1=20&allocation6_2=20&allocation6_3=20&symbol7=VGSH&allocation7_1=20&allocation7_2=20&allocation7_3=20&symbol8=GLD&allocation8_1=20&allocation8_2=10&allocation8_3=10&symbol9=SCHD&allocation9_2=10&symbol10=VNQ&allocation10_3=10) (데이터 문제로 백테스트 기간이 다름)

| 전략 | CARG  | MDD  |
|:---:|:-----:|:----:|
| ⓑ  | 8.09% | -5.23% |
| ⓔ  | 9.48% | -6.42% |
| ⓕ  | 9.16% | -6.36% |

## 다른 시도들 

황금나비의 본래 의도에 맞지는 않지만 장기 채권 대신 고배당주를 섞는 방법(ⓖ), 단기 채권 대신 고배당주를 섞는 방법(ⓗ)도 시도해 보았다. 백테스트 결과는 각각 [여기](https://www.portfoliovisualizer.com/backtest-portfolio?s=y&timePeriod=4&startYear=2010&firstMonth=1&endYear=2019&lastMonth=12&calendarAligned=true&includeYTD=false&initialAmount=10000&annualOperation=0&annualAdjustment=0&inflationAdjusted=true&annualPercentage=0.0&frequency=4&rebalanceType=1&absoluteDeviation=5.0&relativeDeviation=25.0&leverageType=0&leverageRatio=0.0&debtAmount=0&debtInterest=0.0&maintenanceMargin=25.0&leveragedBenchmark=false&reinvestDividends=true&showYield=false&showFactors=false&factorModel=3&benchmark=-1&benchmarkSymbol=SPY&portfolioNames=false&portfolioName1=Portfolio+1&portfolioName2=Portfolio+2&portfolioName3=Portfolio+3&symbol1=SPY&allocation1_1=20&allocation1_2=20&allocation1_3=20&symbol2=VBR&symbol3=QQQ&allocation3_1=20&allocation3_2=20&allocation3_3=20&symbol5=SCHD&allocation5_1=10&allocation5_2=10&allocation5_3=10&symbol6=VGLT&allocation6_1=10&allocation6_2=10&allocation6_3=10&symbol7=VGSH&allocation7_1=20&allocation7_2=20&allocation7_3=20&symbol8=GLD&allocation8_1=20&allocation8_2=10&allocation8_3=10&symbol9=DBC&allocation9_2=10&symbol10=TIP&allocation10_3=10)와 [여기](https://www.portfoliovisualizer.com/backtest-portfolio?s=y&timePeriod=4&startYear=2010&firstMonth=1&endYear=2019&lastMonth=12&calendarAligned=true&includeYTD=false&initialAmount=10000&annualOperation=0&annualAdjustment=0&inflationAdjusted=true&annualPercentage=0.0&frequency=4&rebalanceType=1&absoluteDeviation=5.0&relativeDeviation=25.0&leverageType=0&leverageRatio=0.0&debtAmount=0&debtInterest=0.0&maintenanceMargin=25.0&leveragedBenchmark=false&reinvestDividends=true&showYield=false&showFactors=false&factorModel=3&benchmark=-1&benchmarkSymbol=SPY&portfolioNames=false&portfolioName1=Portfolio+1&portfolioName2=Portfolio+2&portfolioName3=Portfolio+3&symbol1=SPY&allocation1_1=20&allocation1_2=20&allocation1_3=20&symbol2=VBR&symbol3=QQQ&allocation3_1=20&allocation3_2=20&allocation3_3=20&symbol5=SCHD&allocation5_1=10&allocation5_2=10&allocation5_3=10&symbol6=VGLT&allocation6_1=20&allocation6_2=20&allocation6_3=20&symbol7=VGSH&allocation7_1=10&allocation7_2=10&allocation7_3=10&symbol8=GLD&allocation8_1=20&allocation8_2=10&allocation8_3=10&symbol9=DBC&allocation9_2=10&symbol10=TIP&allocation10_3=10)서 찾을 수 있다. 

| 전략 | CARG  | MDD  |
|:---:|:-----:|:----:|
| ⓖ  | 9.03%  | -6.01% |
| ⓗ  | 9.37%  | -5.99% |

## 결론은?

몸통에 TIP를 섞고, 단기 채권에 고배당주를 섞어 커스텀 황금나비를 만들어 보았다. 결과는 [여기](https://www.portfoliovisualizer.com/backtest-portfolio?s=y&timePeriod=4&startYear=1985&firstMonth=1&endYear=2019&lastMonth=12&calendarAligned=true&includeYTD=false&initialAmount=10000&annualOperation=0&annualAdjustment=0&inflationAdjusted=true&annualPercentage=0.0&frequency=4&rebalanceType=1&absoluteDeviation=5.0&relativeDeviation=25.0&leverageType=0&leverageRatio=0.0&debtAmount=0&debtInterest=0.0&maintenanceMargin=25.0&leveragedBenchmark=false&reinvestDividends=true&showYield=false&showFactors=false&factorModel=3&benchmark=-1&benchmarkSymbol=SPY&portfolioNames=false&portfolioName1=Portfolio+1&portfolioName2=Portfolio+2&portfolioName3=Portfolio+3&symbol1=SPY&allocation1_1=20&allocation1_2=20&allocation1_3=20&symbol2=VBR&allocation2_1=20&symbol3=QQQ&allocation3_2=20&allocation3_3=20&symbol5=VGLT&allocation5_1=20&allocation5_2=20&allocation5_3=20&symbol6=VGSH&allocation6_1=10&allocation6_2=10&allocation6_3=10&symbol7=SCHD&allocation7_1=10&allocation7_2=10&allocation7_3=10&symbol8=GLD&allocation8_1=10&allocation8_2=10&allocation8_3=10&symbol9=TIP&allocation9_1=10&allocation9_2=10&symbol10=DBC&allocation10_3=10)와 같다. 

| 전략 | CARG  | MDD  |
|:---:|:-----:|:----:|
| 최종  | 9.55%  | -6.68% |


REF

[게으른 퀀트 / 황금나비 포트폴리오](https://lazyquant.xyz/docs/detail/%EC%9E%90%EC%82%B0%EB%B0%B0%EB%B6%84/12)