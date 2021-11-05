---
description: mqtt 관련 api
---

# MQTT

{% swagger method="post" path="/v1/user/data/room/light/" baseUrl="SERVER_IP:PORT" summary="전등 켜고 끄기" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="String" required="true" %}
Token [token]
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" type="String" required="true" %}
application/x-www-form-urlencoded
{% endswagger-parameter %}

{% swagger-parameter in="body" name="id" type="Integer" required="true" %}
방의 id
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

{% swagger-response status="400: Bad Request" description="" %}
```javascript
{
    "status": 400,
    "detail": "There's no exiting value",
    "data": {}
}
```

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

{% swagger method="get" path="/v1/user/data/room/light/" baseUrl="SERVER_IP:PORT" summary="전등 정보 가져오기" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="String" required="true" %}
Token [token]
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "status": 200,
    "detail": "OK",
    "data": {
        "data":
        [
            {
                "id": 1,
                "name": "방 이름",
                "status": true
            },
            {
                "id": 2,
                "name": "방 이름",
                "status": false
            },
            {
                "id": 3,
                "name": "방 이름",
                "status": true
            },
            {
                "id": 4,
                "name": "방 이름",
                "status": true
            },
            {
                "id": 5,
                "name": "방 이름",
                "status": true
            },
            {
                "id": 6,
                "name": "방 이름",
                "status": true
            }
        ]
    }
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
```javascript
{
    "status": 400,
    "detail": "There's no exiting value",
    "data": {}
}
```

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

{% swagger method="post" path="/v1/user/data/room/light/name/" baseUrl="SERVER_IP:PORT" summary="전등 이름 바꾸기" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" required="true" type="String" %}
Token [token]
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" type="String" required="true" %}
application/x-www-form-urlencoded
{% endswagger-parameter %}

{% swagger-parameter in="body" name="id" type="String" required="true" %}
전등의 ID
{% endswagger-parameter %}

{% swagger-parameter in="body" name="name" type="String" required="true" %}
전등의 새로운 이름
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

{% swagger-response status="400: Bad Request" description="" %}
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

{% swagger method="post" path="/v1/user/data/room/plug/" baseUrl="SERVER_IP:PORT" summary="플러그 켜고 끄기" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="String" required="true" %}
Token [token]
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" type="String" required="true" %}
application/x-www-form-urlencoded
{% endswagger-parameter %}

{% swagger-parameter in="body" name="id" type="Integer" required="true" %}
방의 id
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

{% swagger-response status="400: Bad Request" description="" %}
```javascript
{
    "status": 400,
    "detail": "There's no exiting value",
    "data": {}
}
```

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
    "status": 400,
    "detail": "Some Values are missing",
    "data": {}
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/v1/user/data/room/plug/" baseUrl="SERVER_IP:PORT" summary="플러그 정보 가져오기" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="String" required="true" %}
Token [token]
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "status": 200,
    "detail": "OK",
    "data": {
        "data":
        [
            {
                "id": 1,
                "name": "방 이름",
                "status": true
            },
            {
                "id": 2,
                "name": "방 이름",
                "status": false
            },
            {
                "id": 3,
                "name": "방 이름",
                "status": true
            },
            {
                "id": 4,
                "name": "방 이름",
                "status": true
            },
            {
                "id": 5,
                "name": "방 이름",
                "status": true
            },
            {
                "id": 6,
                "name": "방 이름",
                "status": true
            }
        ]
    }
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
```javascript
{
    "status": 400,
    "detail": "There's no exiting value",
    "data": {}
}
```

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
