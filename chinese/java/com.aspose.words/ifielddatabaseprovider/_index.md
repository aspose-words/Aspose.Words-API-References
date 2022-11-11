---
title: I字段DatabaseProvider
second_title: Aspose.Words for Java API 参考
description:实现此接口以在字段更新时为其提供数据。
type: docs
weight: 640
url: /zh/java/com.aspose.words/ifielddatabaseprovider/
---
```
public interface I字段DatabaseProvider
```

实现此接口以提供数据[字段Database](../../com.aspose.words/fielddatabase)更新时的字段。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [getQueryResult(String fileName, String connection, String query, 字段Database field)](#getQueryResult-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.字段Database-) | 返回查询结果。 |
### getQueryResult(String fileName, String connection, String query, 字段Database field) {#getQueryResult-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.字段Database-}
```
public abstract 字段DatabaseDataTable getQueryResult(String fileName, String connection, String query, 字段Database field)
```


返回查询结果。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 中指定的数据库的完整路径和文件名\\d 字段切换。 |
| connection | java.lang.String | 与指定数据的连接\\c 字段切换。 |
| query | java.lang.String | 查询数据库中指定的 SQL 指令集\\s 字段切换。 |
| field | [字段Database](../../com.aspose.words/fielddatabase) | 正在更新的字段。 |

**退货:**
[字段DatabaseDataTable](../../com.aspose.words/fielddatabasedatatable) - 这[字段DatabaseDataTable](../../com.aspose.words/fielddatabasedatatable)应该用于字段更新的实例。