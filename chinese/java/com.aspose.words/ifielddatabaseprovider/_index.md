---
title: IFieldDatabaseProvider
second_title: Aspose.Words for Java API 参考
description: 实现此接口以在字段更新时为其提供数据。
type: docs
weight: 640
url: /zh/java/com.aspose.words/ifielddatabaseprovider/
---
```
public interface IFieldDatabaseProvider
```

实现此接口以提供数据[FieldDatabase](../../com.aspose.words/fielddatabase)更新时的字段。
## 方法

| 方法 | 描述 |
| --- | --- |
| [getQueryResult(String fileName, String connection, String query, FieldDatabase field)](#getQueryResult-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.FieldDatabase-) | 返回查询结果。 |
### getQueryResult(String fileName, String connection, String query, FieldDatabase field) {#getQueryResult-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.FieldDatabase-}
```
public abstract FieldDatabaseDataTable getQueryResult(String fileName, String connection, String query, FieldDatabase field)
```


返回查询结果。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 中指定的数据库的完整路径和文件名\\d 字段开关。 |
| connection | java.lang.String | 与指定的数据的连接\\c 字段开关。 |
| query | java.lang.String | 查询指定数据库的 SQL 指令集\\s 字段开关。 |
| field | [FieldDatabase](../../com.aspose.words/fielddatabase) | 正在更新的字段。 |

**退货：**
[FieldDatabaseDataTable](../../com.aspose.words/fielddatabasedatatable) - 这[FieldDatabaseDataTable](../../com.aspose.words/fielddatabasedatatable)应用于字段更新的实例。