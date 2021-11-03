# ISugarQueryable

## 概述

- 在查询开始后由query构建的处理对象
- 用于进行查询附加条件的处理

## 方法

### Where

- sql where 子句
- 查询条件

#### 重载(Expression<Func<T, bool>>)

##### 泛型 

- ORM实体对象

##### 参数

| 参数名     | 描述 | 类型                      | 必须 | 举例                                  | 备注 |
| ---------- | ---- | ------------------------- | ---- | ------------------------------------- | ---- |
| expression |      | Expression<Func<T, bool>> | true | it=> SqlFunc.EqualsNull(it.Name,null) |      |

##### 返回值

- [ISugarQueryable\<T\>](#ISugarQueryable)

### OrderBy

- sql OrderBy子句 

- 查询排序

####  重载 (Expression<Func<T, object>>, OrderByType type = OrderByType.Asc)

##### 泛型 

- ORM实体对象

##### 参数

| 参数名     | 描述 | 类型                      | 必须 | 默认值                                    | 举例                                  | 备注 |
| ---------- | ---- | ------------------------- | ---- | ----------------------------------------- | ------------------------------------- | ---- |
| expression |      | Expression<Func<T, bool>> | true |                                           | it=> SqlFunc.EqualsNull(it.Name,null) |      |
| type       |      |                           |      | [OrderByType](..\Enum\OrderByType.md).Asc |                                       |      |

##### 返回值

- [ISugarQueryable\<T\>](#ISugarQueryable)



