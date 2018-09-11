1. 获取访问令牌

浏览器请求：

http://localhost:8080/oauth/authorize?client_id=clientapp&redirect_uri=http://localhost:9001/callback&response_type=token&scope=read_userinfo&state=abc

响应案例：

http://localhost:9001/callback#access_token=0406040a-779e-4b5e-adf1-bf2f02031e83&token_type=bearer&state=abc&expires_in=119

2. 调用API

curl -X GET http://localhost:8080/api/userinfo -H "authorization: Bearer 0406040a-779e-4b5e-adf1-bf2f02031e83"

案例响应：

{
    "name": "niuniu",
    "email": "bobo@spring2go.com"
}