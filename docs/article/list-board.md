# 获取版面文章、主题列表

## URL

<u>/api/article/list</u>

## 请求方式
HTTP GET

## 请求参数

| 参数字段    | 是否必选  | 说明         |
| :--------- | :------: | :---------- |
| type       | true     | board |
| board      | true     | 版面名 |
| btype      | true     | <u>t</u> 为主题模式，其他为一般模式|
| count      | false    | 希望查询的文章数量，默认为20篇。实际文章数可能小于 count，所以最终返回文章数以实际情况为准 |
| page       | false    | 分页数，从 0 开始的整数，数字越小越接近最新发表的文章 |
| startnum   | false    | 从该版所有文章的第几篇起返回，取值不小于1。默认为从最新文章起，倒推 count 篇，若总文章不足 count 篇，则从第一篇（最老一篇）开始输出。|
| userid     | true     | 当前登录用户的 ID |
| sessid     | true     | 当前用户的 session ID |
| appkey     | true     | 当前使用的 APP 标识 |

## 返回结果（示例）

### 一般模式

```JSON
{
    "errcode":0,
    "articlelist":[
        {
            "type":0,
            "aid":1419314662,
            "tid":1419314662,
            "th_num":1,
            "mark":0,
            "num":8,
            "board":"sysop",
            "title":"你说的太对了",
            "author":"IronBlood"
        },
        {
            "type":0,
            "aid":1419314676,
            "tid":1419314676,
            "th_num":1,
            "mark":0,
            "num":9,
            "board":"sysop",
            "title":"我竟无言以对",
            "author":"IronBlood"
        },
        { ... }
    ]
}
```

### 主题模式

```JSON
{
    "errcode":0,
    "articlelist":[
        {
            "type":1,
            "aid":1425875627,
            "tid":1425875627,
            "th_num":5,
            "mark":36,
            "num":8963,
            "th_size":90029,
            "th_commenter":[
                "zuojian",
                "zousuifeng",
                "Qinghai"
            ],
            "board":"sysop",
            "title":"第十二届兵马俑BBS乡音乡情足球联赛报名通知",
            "author":"maxif"
        },
        {
            "type":1,
            "aid":1425977944,
            "tid":1425977944,
            "th_num":9,
            "mark":0,
            "num":8968,
            "th_size":541,
            "th_commenter":[
                "hyclnan",
                "ffddmm",
                "Flymilk",
                "zixu",
                "Like",
                "ArthurF",
                "KnightX"
            ],
            "board":"sysop",
            "title":"[转载] 关于在全校计算机上安装360天擎系统的通知",
            "author":"nic"
        },
        { ... }
    ]
}
```
## 注意事项
