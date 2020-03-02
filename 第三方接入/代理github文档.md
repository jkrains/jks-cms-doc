# 代理github 文档

支持文档内容直接来自github， 用户可以把自己公开的文档使用markdown 语法来编写。然后托管到github上。

## github项目配置

**请求PATH**

-  `gh-docs`

**支持接口**

- `getList()`,
- `getItemById()`
- `updateItemById()`  
- `deleteItemById()`
- `getTotals()`



**参数实例**

```{json
{
    "_id":"122134124242",
    "cid": "334339f3eedde444",
    "tid": "333343434343434",
    "project": "volley",
    "branch": "v1.0.2",
    "overview": "此版本，描述",
    "tags":["3242424", "3242424242"],
    "token": "123344578867878783443ffff",
    "hasToken": true
}
```



**参数说明**

| 字段     | 是否必须 | 类型     | 说明                                                         |
| -------- | -------- | -------- | ------------------------------------------------------------ |
| _id      | 是       | String   | 唯一标识，由服务器产生                                       |
| cid      | 是       | String   | 文件                                                         |
| tid      | 是       | String   | 分组id                                                       |
| project  | 是       | String   | 项目名称，对应在github的项目名称                             |
| branch   | 是       | String   | 分支名称，一般携带版本号，对应在github的分支名称。           |
| overview | 否       | String   | 概述，用户标注                                               |
| tags     | 否       | String[] | 标签，用户设置                                               |
| token    | 否       | String   | 私钥令牌， 用户可以在其账号设置，然后填写，本字段为选填，如果不填写，则可以访问github的公有资源，但每天的调用次数受限制。该字段只可设置，不可回读（为了用户的信息安全）。 |
| hasToken | 是       | boolean  | 用户设置完token后，该字段表示用户是否已经设置过token了。     |

**注意**

