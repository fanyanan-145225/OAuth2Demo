1. 获取访问令牌

curl -X POST "http://localhost:8080/oauth/token" --user clientdevops:789 -d "grant_type=client_credentials&scope=devops"

响应案例：

{
    "access_token": "776b162a-949e-4dcb-b16b-9985e8171dc0",
    "token_type": "bearer",
    "expires_in": 43188,
    "scope": "devops"
}
2. 调用API

curl -X GET http://localhost:8080/api/userlist -H "authorization: Bearer 776b162a-949e-4dcb-b16b-9985e8171dc0"

案例响应：

[
    {
        "name": "niuniu",
        "email": "niuniu@spring2go.com"
    },
    {
        "name": "eric",
        "email": "eric@spring2go.com"
    },
    {
        "name": "franky",
        "email": "franky@spring2go.com"
    }
]
