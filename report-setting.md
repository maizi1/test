## 获取USER列表

#### **GET**  /a/userList

| 请求参数 | 类型   |          |
| -------- | ------ | -------- |
| size     | number | 每页条数 |
| page     | number | 页数     |

| 响应    |                   |              |
| ------- | ----------------- | ------------ |
| code    | number            | 自定义状态码 |
| message | string：’succeed‘ | 提示消息     |
| total   | number            | 数据总条数   |
| data    | array             |              |

| data       |      |      |
| ---------- | ---- | ---- |
| id         |      |      |
| pubname    |      |      |
| createtime |      |      |
| open       |      |      |

## 获取app列表

#### **GET**  /a/channelList/{uid}

| 响应    |                   |              |
| ------- | ----------------- | ------------ |
| code    | number            | 自定义状态码 |
| message | string：’succeed‘ | 提示消息     |
| total   | number            | 数据总条数   |
| data    | array             |              |

| data        |      |      |
| ----------- | ---- | ---- |
| id          |      |      |
| uid         |      |      |
| source      |      |      |
| channel     |      |      |
| channelname |      |      |
| proportion  |      |      |
| buffer      |      |      |
| switch      |      |      |
| reset       |      |      |
| createtime  |      |      |

