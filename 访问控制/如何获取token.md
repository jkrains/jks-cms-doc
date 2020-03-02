

# 如何获取token

> token是HTTP API接口与服务器交互的重要依据，通过token服务器判断当前请求的合法性，在 api 接口没有特殊说明时，API的请求都需要token。token的获取是通过密钥凭证或者用户账户登录后可返回token， 密钥凭证为应用程序的重要访问账号，不可透露给他人。token和具体的权限相关联，通过账号登录获取token,请参考账号登录章节，本章如下描述通过应用程序获取token的方法。

**请求PATH**

-  `/token`

**http请求方式**

- post

**body参数**

| 字段名称   | 变量名   | 必填 | 类型   | 实例值                           | 描述                                  |
| ---------- | -------- | ---- | ------ | -------------------------------- | ------------------------------------- |
| 应用程序Id | appId    | 是   | String | b025cdb6a7e54167d42eeb35cfa      | 应用程序的唯一标识                    |
| 密钥Id     | secretId | 是   | String | 8b195954a2474040rr7b6aab82cc2177 | 密钥id， 可以理解某个应用程序的子账号 |
| 密钥       | secretId | 是   | String | L8nXW%oVTv%725fddfgSTgSBU7p7kI8A | 密钥值                                |
**示例**

```json
{
    "appId": "b025cdb6a7e5412ed42eeb35cfa",
    "secretId": "8b195964a2474040946b6aab82cc2177",
    "secretKey": "L8nXW%oVTv%756oewm4STgSBU7p7kI8A"
}
```
**成功返回结果**

```json
{
    "scode": 0,
    "msg": "ok",
    "data": {
        "token": "fw3r888888wr555555r67888w8888rw"
    }
}
```
**失败返回结果**

```json
{
    "scode": -34454544,
    "msg": "not found"
}
```

**失败错误码(scode)**

| 定义 | 含义|
| --------------------- | ----------------- |
| INTERVAL_SERVER_ERORR | 为服务器内部出错，可以通过msg拿到详细的错误描述 |
| ERR_ILLEGAL_ARG       | 非法错误参数  |
| ERROR                 | 通用错误  |