# ConnectionConfig

## 概述

- 用于初始化SqlSugarClient时所用的配置

## 属性

| 属性                      | 描述                 | 类型                                                      | 必须 | 备注                                                         |
| ------------------------- | -------------------- | --------------------------------------------------------- | ---- | ------------------------------------------------------------ |
| ConfigId                  | 连接唯一识别码       | dynamic                                                   |      | 用于在配置了多个数据库连接时区分各个连接                     |
| DbType                    | 数据库类型           | [DbType](../Enum/DbType.md)                               | true |                                                              |
| ConnectionString          | 数据库连接字符串     | string                                                    | true |                                                              |
| IsAutoCloseConnection     | 是否自动关闭连接     | bool                                                      |      |                                                              |
| InitKeyType               | 默认属性             | [InitKeyType](../Emum/InitKeyType.md)                     |      | 从哪里初始化每个数据表的主键和自增                           |
| LanguageType              | 错误提示时使用的语言 | [LanguageType](../Enum/LanguageType.md)                   |      | 例如中文                                                     |
| ConfigureExternalServices | 配置外部服务         | [ConfigureExternalServices](#ConfigureExternalServices)   |      | 配置外部服务以取代默认服务，例如Redis存储。                  |
| SlaveConnectionConfigs    | 从连接配置           | List<[SlaveConnectionConfigs](SlaveConnectionConfigs.md)> |      | /// If SlaveConnectionStrings has value,ConnectionString is write operation, SlaveConnectionStrings is read operation.<br/>        /// All operations within a transaction is ConnectionString<br />推测为配置该数据库连接是否为只读连接 |
| MoreSettings              | 更多设置             | [MoreSettings](ConnMoreSettings.md)                       |      |                                                              |
| IndexSuffix               | 索引后缀             | string                                                    |      | 未知                                                         |
| AopEvents                 |                      | [AopEvents](#AopEvents)                                   |      |                                                              |

# AopEvents

### 概述

- 进行操作时触发的事件

## 属性

| 属性           | 描述     | 类型                             | 必须 | 备注                   |
| -------------- | -------- | -------------------------------- | ---- | ---------------------- |
| OnLogExecuting | 执行日志 | Action<string, SugarParameter[]> |      | 推测可用于输出日志信息 |

# ConfigureExternalServices





