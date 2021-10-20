# Mock-Up

{% swagger method="get" path="/mockup/video" baseUrl="SERVER_IP:PORT" summary="영상 리스트 가져오기" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "status": 200,
    "detail": "OK",
    "data": {
        "article": [
            {
                "name": "1",
                "video": "VIDEO_URL"
            },
            {
                "name": "2",
                "video": "VIDEO_URL"
            },
            {
                "name": "3",
                "video": "VIDEO_URL"
            }
        ]
    }
}
```
{% endswagger-response %}
{% endswagger %}
