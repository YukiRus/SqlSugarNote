# SqlSugarClient

## 概述

- SqlSugar的基类，实例化后提供对数据库的各种查询操作的封装

## 属性

| 属性                    | 描述         | 类型                                             | 必须 | 备注                                                         |
| ----------------------- | ------------ | ------------------------------------------------ | ---- | ------------------------------------------------------------ |
| CurrentConnectionConfig | 当前连接配置 | [ConnectionConfig](Entities\ConnectionConfig.md) |      | 可以通过这个属性.配置项属性来修改配置<br />禁止修改<br />  DbType <br />  ConnectionString |

## 方法

### SqlSugarClient

- 构造函数

#### 重载(ConnectionConfig)

##### 参数

| 参数名 | 描述 | 类型                                             | 必须 | 举例 | 备注 |
| ------ | ---- | ------------------------------------------------ | ---- | ---- | ---- |
| config |      | [ConnectionConfig](Entities/ConnectionConfig.md) |      |      |      |

##### 调用举例

```C#
SqlSugarClient db = new SqlSugarClient(new ConnectionConfig()
{
    ConnectionString = "Server=.xxxxx",// 连接符字串
    DbType = DbType.SqlServer, // 数据库类型
    IsAutoCloseConnection = true// 指定数据库是否自动关闭，如果为false则需要手动关闭
});
```

#### 重载(List\<ConnectionConfig\>)

##### 参数

| 参数名  | 描述 | 类型                                                   | 必须 | 举例 | 备注 |
| ------- | ---- | ------------------------------------------------------ | ---- | ---- | ---- |
| configs |      | List<[ConnectionConfig](Entities/ConnectionConfig.md)> |      |      |      |



### Queryable

#### 重载  [ISugarQueryable\<T\>](Interface\IQueryable.md) ()

##### 泛型T

- 应为ORM实体类

