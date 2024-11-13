# 3.1.2 Computer System Collection

## 命令功能

> 查询计算机系统资源集合。

## 命令格式

> 操作类型: **GET**
> 
> URL: https://{device_ip}/redfish/v1/Systems
> 
> 请求头: 无
> 
> 请求消息体: 无

## 参数说明

> **表3-4 公共固定资源参数说明**
> | 参数 | 参数说明 | 取值 |
> |------|----------|------|
> | device_ip | 登录设备的IP地址 | IPv4或IPv6地址 |

## 使用指南

> 无

## 使用实例

> 请求样例:
> 
> GET https://{device_ip}/redfish/v1/Systems
> 
> 请求头: 无
> 
> 请求消息体: 无
> 
> 响应样例:
> 
> ```json
> {
>     "@odata.context": "/redfish/v1/$metadata#ComputerSystemCollection.ComputerSystemCollection",
>     "@odata.id": "/redfish/v1/Systems",
>     "@odata.type": "#ComputerSystemCollection.ComputerSystemCollection",
>     "Members": [
>         {
>             "@odata.id": "/redfish/v1/Systems/System1"
>         },
>         {
>             "@odata.id": "/redfish/v1/Systems/System2"
>         }
>     ],
>     "Members@odata.count": 2
> }
> ```

## 输出说明

> **表 3-5 Collection Properties 输出字段说明**

| 字段                  | 类型    | 只读 | 说明                                                                 |
|-----------------------|---------|------|----------------------------------------------------------------------|
| @odata.context        | 字符串  | 是   | 参考 ODATA 属性部分                                                 |
| @Redfish.CollectionCapabilities | 对象   | 是   | 参考 CollectionCapabilities 注解。此注解仅在 Systems Collection 和 ResourceZone 实例响应中存在。 |
| @odata.id             | 字符串  | 是   | 参考 ODATA 属性部分                                                 |
| @odata.type           | 字符串  | 是   | 参考 ODATA 属性部分                                                 |
| @odata.etag           | 字符串  | 是   | 参考 ODATA 属性部分                                                 |
| Oem                   | 对象    | 否   | 参考 Resource Complex Types 部分。若实现了 OEM 扩展，响应中将包含此字段。|
| Members               | 数组    | 是   | 包含此集合中的成员                                                  |
| Members@odata.count   | 数字    | 是   | 集合成员的数量                                                      |
| Name                  | 字符串  | 是   | 集合的名称                                                           |
| Description           | 字符串  | 是   | 提供资源的描述                                                       |


## 备注

> 无
