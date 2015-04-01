# 获取同主题文章列表

## URL

<u>/api/article/list</u>

## 请求方式
HTTP GET

## 请求参数

| 参数字段    | 是否必选  | 说明         |
| :--------- | :------: | :---------- |
| type       | true     | thread |
| board      | true     | 版面名 |
| thread     | true     | 主题 ID |
| count      | false    | 希望查询的文章数量，默认为全部输出 |
| startnum   | false    | 确定从该版的第几个主题起返回，取值不小于1。默认为从最新文章起，倒推 count 篇，若总文章不足 count 篇，则从第一篇（最老一篇）开始输出。|
| userid     | true     | 当前登录用户的 ID |
| sessid     | true     | 当前用户的 session ID |
| appkey     | true     | 当前使用的 APP 标识 |

## 返回结果（示例）

```JSON
{
    "errcode":0,
    "articlelist":[
        {
            "type":0,
            "aid":1419314676,
            "tid":1419314676,
            "th_num":1,
            "mark":0,
            "secstr":"0",
            "board":"sysop",
            "title":"我竟无言以对",
            "author":"IronBlood"
        },
        { ... }
    ]
}
```

## 注意事项
