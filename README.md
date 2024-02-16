# OnlineClass

## 数据格式
服务端与客户端之间传输的大体数据格式如下：
```json
{
    "type": event_type,
    "time": event_time,
    "content": {
        "type": content_type,
        "value": value
    }
}
```
其中`event_type`为事件类型，`event_time`为事件时间，`event_content`为事件内容。`event_type`和`event_time`均为`string`类型.`event_content`类型请在[事件类型](#事件类型)中查询.

## 事件类型
规定的事件类型如下：
- Connect
- Connected
- Disconnected
- ScreenUpdate
- OpenStudentMicrophone
- CloseStudentMicrophone
- OpenStudentCamera
- CloseStudentCamera
- ClassBegin
- ClassOver
### 事件介绍
#### Connect
数据格式：
```json
{
    "type": "Connect",
    "time": time,
    "content": {
        "type": "json",
        "value": {
            "StudentInfo":{
                "name": StudentName
            }
        }
    }
}
```


