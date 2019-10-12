# report-admin-in

#### 登录

**POST**	/a/login

###### 请求参数

| 参数 | 类型   | 备注 |
| ---- | ------ | ---- |
| name | string |      |
| pwd  | string |      |

###### 响应体

| 参数    | 类型   | 备注     |
| ------- | ------ | -------- |
| code    | number | 请求状态 |
| message | string | 提示消息 |
| data    | object |          |

data

| 参数     | 类型                                                   | 备注                              |
| -------- | ------------------------------------------------------ | --------------------------------- |
| channels | array [{id:number,name:string,}]                       |                                   |
| user     | object {id:number, status:number, channelName: string} | status字段的值为0或1，0为禁止登录 |

#### 数据

**GET**	/a/u/channelData

| 参数    | 类型   | 备注                                                         |
| ------- | ------ | ------------------------------------------------------------ |
| uid     | number | 用户id                                                       |
| cid     | number | 渠道id 可选，带有渠道id时为单个渠道数据，不带时为账号下全部数据 |
| page    | number |                                                              |
| size    | number |                                                              |
| startAt | number | 开始日期 毫秒                                                |
| endAt   | number | 结束日期 毫秒                                                |

##### 响应

| 参数    | 类型   | 备注     |
| ------- | ------ | -------- |
| code    | number | 请求状态 |
| message | string | 提示消息 |
| data    | object |          |

data

| 参数    | 类型              | 备注                     |
| ------- | ----------------- | ------------------------ |
| total   | number            | 总数                     |
| startAt | date              | 能查到的第一条数据的日期 |
| results | array [...object] |                          |

results

| 参数    | 类型        | 备注 |
| ------- | ----------- | ---- |
| type    | string      |      |
| channel | string      |      |
| pv      | [...number] | 中间如有缺失数据补零     |
| uv      | [...number] | 中间如有缺失数据补零     |
| income  | [...number] | 中间如有缺失数据补零     |

