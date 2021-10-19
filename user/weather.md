---
description: FineDust, Weather
---

# Weather

{% swagger method="get" path="/v1/user/data/finedust/" baseUrl="SERVER_IP:PORT" summary="미세먼지 정보 저장" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" required="true" %}
Token [token]
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" required="true" %}
application/x-www-form-urlencoded
{% endswagger-parameter %}

{% swagger-parameter in="body" name="firstCityName" required="true" %}
도시이름 - 1
{% endswagger-parameter %}

{% swagger-parameter in="body" name="lastCityName" required="true" %}
도시이름 - 2
{% endswagger-parameter %}

{% swagger-parameter in="body" name="fineDustValue" required="true" %}
좋음 - 보통 - 나쁨 - 매우나쁨
{% endswagger-parameter %}

{% swagger-parameter in="body" name="fineDust" required="true" %}
미세먼지 값
{% endswagger-parameter %}
{% endswagger %}
