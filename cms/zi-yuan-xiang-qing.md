**模块列表**

接口： /resources/modules

方法：POST

示例： [http://player.roobo.net/resources/modules](http://player.roobo.net/resources/modules)

请求参数

```
{
  "appId" : "EvXLUN3xtyON74KY",
  "token" : "786203ce01256d1d590e2d0a1c1f11b62076",
  "clientId" : "10110000002003C7",
  "tags" : []
}
```

其中

| 参数 | 类型 | 可选 | 意义 |
| :--- | :--- | :--- | :--- |
| appId | string | 必选 | 应用ID |
| clientId | string | 可选 | 用于绑定收藏的用户ID |
| tags\[\] | string | 必选 | 过滤标签 |

返回值

```
{
    "result": 0,
    "msg": "success",
    "data": {
        "total": 2,
        "modules": [
            {
                "id": 5,
                "name": "gagaagaga",
                "icon": "http://dwn.roo.bo/voices/songs/test/31e81c7b2323694c53b491691f20998e.jpg",
                "attr": "mod",
                "description": "",
                "contents": [
                    {
                        "id": 6,
                        "type": "audio",
                        "content": "28537",
                        "name": "hello content",
                        "img": "",
                        "tags": []
                    }
                ]
            },
            {
                "id": 1,
                "name": "4444",
                "icon": "http://dwn.roo.bo/voices/songs/test/31e81c7b2323694c53b491691f20998e.jpg",
                "attr": "ad",
                "description": "",
                "contents": [
                    {
                        "id": 1,
                        "type": "ad",
                        "content": "1",
                        "name": "喜羊羊",
                        "img": "gaga",
                        "tags": [],
                        "list": [
                            {
                                "id": 1,
                                "type": "album",
                                "content": "8075",
                                "name": "",
                                "img": "",
                                "description": ""
                            }
                        ]
                    }
                ]
            }
        ]
    }
}
```

各返回值意义如下



| 返回值 | 类型 | 意义 |
| :--- | :--- | :--- |
| data.total | int | 模块总数量 |
| data.modules\[\].id | string | 模块id |
| data.modules\[\].name | string | 模块名字 |
| data.modules\[\].attr | string | 模块类型：ad-广告模块；mod-普通模块； |
| data.modules\[\].description | string | 模块介绍 |
| data.modules\[\].icon | string | 模块图标 |
| data.modules\[\].contents\[\].id | string | 内容ID |
| data.modules\[\].contents\[\].name | string | 内容名称 |
| data.modules\[\].contents\[\].description | string | 内容详细描述 |
| data.modules\[\].contents\[\].img | string | 内容图片 |
| data.modules\[\].contents\[\].type | string | 内容类型： album-歌单；ad-广告内容；audio-歌曲； |
| data.modules\[\].contents\[\].tags\[\] | string | 运营标识：new，hot；年龄标识：one,two,three; |
| data.modules\[\].contents\[\].detail | array | 歌单、歌曲的详细信息 |
| data.modules\[\].contents\[\].lists\[\].id | string | 广告id |
| data.modules\[\].contents\[\].lists\[\].name | string | 广告名称 |
| data.modules\[\].contents\[\].lists\[\].type | string | 广告类型 |
| data.modules\[\].contents\[\].lists\[\].content | string | 广告内容 |
| data.modules\[\].contents\[\].lists\[\].img | string | 广告图片 |
| data.modules\[\].contents\[\].lists\[\].description | string | 广告描述 |


