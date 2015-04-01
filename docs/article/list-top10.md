# 获取十大热门话题列表

## URL

<u>/api/article/list</u>

## 请求方式
HTTP GET

## 请求参数

| 参数字段    | 是否必选  | 说明         |
| :--------- | :------: | :----------- |
| type       | true     | top10        |

## 返回结果（示例）

```JSON
{
    "errcode":0,
    "articlelist":[
        {
            "type":1,
            "aid":0,
            "tid":1414812201,
            "th_num":1,
            "mark":0,
            "secstr":"0",
            "board":"sysop",
            "title":"test",
            "author":""
        },
        {
            "type":1,
            "aid":0,
            "tid":1414854530,
            "th_num":1,
            "mark":0,
            "secstr":"0",
            "board":"sysop",
            "title":"zhengwen",
            "author":""
        }
    ]
}
```

## 注意事项
