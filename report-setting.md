## 获取USER列表

#### **GET**  /a/userList

| 请求参数 | 类型   | 备注     |
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

| 响应    | 类型              | 备注         |
| ------- | ----------------- | ------------ |
| code    | number            | 自定义状态码 |
| message | string：’succeed‘ | 提示消息     |
| total   | number            | 数据总条数   |
| data    | array             |              |

| data        | 类型 | 备注 |
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

## 更新用户 Open 状态
#### **PATCH**  /a/userOpen/{id}

| 参数 | 类型   | 备注   |
| ---- | ------ | ------ |
| open | number | 1 or 0 |

| 响应    | 类型   | 备注                |
| ------- | ------ | ------------------- |
| code    | number | 修改成功时，值为200 |
| message | string | 提示消息            |

## 更新 channel

#### **PATCH** /a/channel

| 参数       | 类型             | 备注 |
| ---------- | ---------------- | ---- |
| id         | number           | 必选 |
| reset      | number: 1 or 0   | 可选 |
| switch     | number: 1 or 0   | 可选 |
| buffer     | number: 1-100    | 可选 |
| proportion | number : 1 - 100 | 可选 |

| 响应    | 类型   | 备注                |
| ------- | ------ | ------------------- |
| code    | number | 修改成功时，值为200 |
| message | string | 提示消息            |

## 新增 channel

#### **POST** /a/channel

| 参数        | 类型   | 备注 |
| ----------- | ------ | ---- |
| id          | number | 必选 |
| source      | string | 必选 |
| channel     | string | 必选 |
| channelname | string | 必选 |
| proportion  | number | 必选 |
| buffer      | number | 必选 |
| switch      | number | 必选 |
| reset       | number | 必选 |

| 响应    | 响应   | 备注     |
| ------- | ------ | -------- |
| code    | number |          |
| message | string | 提示消息 |

## 新增 user

#### **PSOT** /a/user

| 参数     | 类型   | 备注 |
| -------- | ------ | ---- |
| id       | number |      |
| pubname  | string |      |
| password | string |      |

| 响应    | 响应   | 备注     |
| ------- | ------ | -------- |
| code    | number |          |
| message | string | 提示消息 |

