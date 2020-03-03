# 接入github

支持文档内容直接来自github， 用户可以把自己公开的文档使用markdown 语法来编写。然后托管到github上。目前只支持从github上读取内容。

## github项目信息

**请求PATH**

-  `/gh-docs`

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
    "username": "jkrains",
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
| username | 是       | String   | 用户在github上的账户名称必填                                 |
| project  | 是       | String   | 项目名称，对应在github的项目名称                             |
| branch   | 是       | String   | 分支名称，一般携带版本号，对应在github的分支名称。           |
| overview | 否       | String   | 概述，用户标注                                               |
| tags     | 否       | String[] | 标签，用户设置                                               |
| token    | 否       | String   | 私钥令牌， 用户可以在其账号设置，然后填写，本字段为选填，如果不填写，则可以访问github的公有资源，但每天的调用次数受限制。该字段只可设置，不可回读（为了用户的信息安全）。 |
| hasToken | 是       | boolean  | 用户设置完token后，该字段表示用户是否已经设置过token了。     |

**注意**

如果用户未认证，及上述token未填写，则默认每小时最多可以请求60次。且只能访问公开的信息。

如果用户填写了token, 并认证通过， 则每小时可以访问5000次。并且可以访问用户的私有资源。



## 获取项目目录

**请求PATH**

- `/gh-data/content/:username/:project/:branch`

**请求类型**

- `get`

**说明**

如上PATH所示， `/gh-data/content`固定，为PATH的前缀， username为用户在github的用户名，project为项目名称， branch为用户的项目分支，一般表示版本号。

**示例**

```json
/gh-data/content/jkrains/jks-cms-doc/v1
```



## 获取文件元数据

**请求PATH**

- `/gh-data/raw/:username/:project/:branch`

**请求类型**

- `get`

**说明**

如上PATH所示， `/gh-data/raw`固定，为PATH的前缀， username为用户在github的用户名，project为项目名称， branch为用户的项目分支，一般表示版本号。

**示例**

```json
/gh-data/raw/jkrains/jks-cms-doc/v1
```

