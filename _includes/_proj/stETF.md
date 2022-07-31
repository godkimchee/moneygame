{% for tg in include.tickers %}

{% assign etf = site.data.proj.stETF | where:"TICKER", tg | first %}

{{etf.NAME}} 【{{etf.TICKER}}】
* ETF 정보: [운용사 제공 정보]( {{ etf.URL }}), [네이버 제공 정보]({{ etf.INFO.NAVER.URL }})
* 추종 지수 : [{{ etf.IDX.NAME }}]({{ etf.IDX.LINK}})
* 시가총액 : 현재 {{ etf.CAP }} 억원
* 설명 : {{ etf.INFO.NAVER.DESC }} (REF: 네이버 금융)

{% endfor %}
