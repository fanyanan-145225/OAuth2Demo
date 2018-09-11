1. 获取访问令牌

curl -X POST --user clientapp:112233 http://localhost:8080/oauth/token -H "accept: application/json" -H "content-type: application/x-www-formurlencoded" -d "grant_type=password&username=niuniu&password=fyn&scope=read_userinfo"

响应案例：

{
    "access_token": "a8578776-16df-45a0-b3d1-20b49a252bbe",
    "token_type": "bearer",
    "expires_in": 43199,
    "scope": "read_userinfo"
}
2. 调用API

curl -X GET http://localhost:8080/api/userinfo -H "authorization: Bearer 58a02fd5-87f5-44ff-bbdd-d429cf6a2f60"

案例响应：

{
    "name": "niuniu",
    "email": "niuniu@spring2go.com"
}