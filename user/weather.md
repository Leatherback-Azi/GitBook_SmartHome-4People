---
description: FineDust, Weather
---

# Weather

{% swagger method="post" path="/v1/user/data/finedust/" baseUrl="SERVER_IP:PORT" summary="미세먼지 정보 저장" %}
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

{% swagger-response status="200: OK" description="" %}
저장에 성공 하였을 때

```javascript
{
    "status": 200,
    "detail": "OK",
    "data": {}
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
일부 값이 전달되지 않았을 때

```javascript
{
    "status": 400,
    "detail": "Some Values are missing",
    "data": {}
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}
토큰이 유효하지 않을 때

```javascript
{
    "detail": "Invalid token." 
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/v1/user/data/finedust/" baseUrl="SERVER_IP:PORT" summary="미세먼지 정보 가져오기" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" required="true" %}
Token [token]
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
성공적으로 불러 왔을 시

```javascript
{
    "status": 200,
    "detail": "OK",
    "data": {
        "firstCityName": "대구광역시",
        "lastCityName": "유가읍",
        "fullCityName": "대구광역시 유가읍",
        "fineDustValue": "나쁨",
        "fineDust": 400
    }
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
일부 값이 전달되지 않았을 때

```javascript
{
    "status": 400,
    "detail": "Some Values are missing",
    "data": {}
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}
```javascript
{
    "detail": "Invalid token." 
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/v1/user/data/weather/" baseUrl="SERVER_IP:PORT" summary="날씨 정보 등록하기" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="String" required="true" %}
application/x-www-form-urlencoded
{% endswagger-parameter %}

{% swagger-parameter in="body" name="city" type="String" required="true" %}
도시 이름
{% endswagger-parameter %}

{% swagger-parameter in="body" name="weather" type="String" required="true" %}
날씨
{% endswagger-parameter %}

{% swagger-parameter in="body" name="temperature" type="Intager" required="true" %}
온도
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "status": 200,
    "detail": "OK",
    "data": {}
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}
```javascript
{
    "detail": "Invalid token." 
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/v1/user/data/weather/" baseUrl="SERVER_IP:PORT" summary="날씨 정보 가져오기" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="String" required="true" %}
Token [token]
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
성공적으로 가져왔을 때

```javascript
{
    "status": 200,
    "detail": "OK",
    "data": {
        "city": "대구광역시 유가읍",
        "weather": "맑음",
        "temperature": 38,
    }
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}
```javascript
{
    "detail": "Invalid token." 
}
```
{% endswagger-response %}
{% endswagger %}
