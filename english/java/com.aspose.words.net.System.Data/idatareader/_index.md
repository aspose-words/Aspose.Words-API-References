---
title: IDataReader
second_title: Aspose.Words for Java API Reference
description: 提供一种读取通过在数据源处执行命令获得的一个或多个只进结果集流的方法，由访问关系数据库的 .NET Framework 数据提供程序实现。
type: docs
weight: 34
url: /zh/java/com.aspose.words.net.system.data/idatareader/
---

**All Implemented 界面s:**
[com.aspose.words.net.System.Data.IDataRecord](../../com.aspose.words.net.system.data/idatarecord)
```
public interface IDataReader extends System.Data.IDataRecord
```

提供一种读取通过在数据源处执行命令获得的一个或多个只进结果集流的方法，由访问关系数据库的 .NET Framework 数据提供程序实现。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [close()](#close--) | 关闭[IDataReader](../../com.aspose.words.net.system.data/idatareader)目的。 |
| [getDepth()](#getDepth--) | 获取一个值，该值指示当前行的嵌套深度。 |
| [getRecordsAffected()](#getRecordsAffected--) | 获取通过执行 SQL 语句更改、插入或删除的行数。 |
| [getSchemaTable()](#getSchemaTable--) | 返回一个[DataTable](../../com.aspose.words.net.system.data/datatable)描述列元数据的[IDataReader](../../com.aspose.words.net.system.data/idatareader). |
| [isClosed()](#isClosed--) | 获取一个值，该值指示数据读取器是否已关闭。 |
| [nextResult()](#nextResult--) | 读取批处理 SQL 语句的结果时，将数据读取器推进到下一个结果。 |
| [read()](#read--) | 推进[IDataReader](../../com.aspose.words.net.system.data/idatareader)到下一条记录。 |
### close() {#close--}
```
public abstract void close()
```


关闭[IDataReader](../../com.aspose.words.net.system.data/idatareader)目的。

### getDepth() {#getDepth--}
```
public abstract int getDepth()
```


获取一个值，该值指示当前行的嵌套深度。

**退货:**
int - 嵌套级别。
### getRecordsAffected() {#getRecordsAffected--}
```
public abstract int getRecordsAffected()
```


获取通过执行 SQL 语句更改、插入或删除的行数。

**退货:**
int - 更改、插入或删除的行数；如果没有行受到影响或语句失败，则为 0；和 -1 用于 SELECT 语句。
### getSchemaTable() {#getSchemaTable--}
```
public abstract System.Data.DataTable getSchemaTable()
```


返回一个[DataTable](../../com.aspose.words.net.system.data/datatable)描述列元数据的[IDataReader](../../com.aspose.words.net.system.data/idatareader).

**退货:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - 一个[DataTable](../../com.aspose.words.net.system.data/datatable)描述列元数据。
### isClosed() {#isClosed--}
```
public abstract boolean isClosed()
```


获取一个值，该值指示数据读取器是否已关闭。

**退货:**
boolean - 如果数据读取器已关闭，则为 true；否则为假。
### nextResult() {#nextResult--}
```
public abstract boolean nextResult()
```


读取批处理 SQL 语句的结果时，将数据读取器推进到下一个结果。

**退货:**
boolean - 如果有更多行，则为 true；否则为假。
### read() {#read--}
```
public abstract boolean read()
```


推进[IDataReader](../../com.aspose.words.net.system.data/idatareader)到下一条记录。

**退货:**
boolean - 如果有更多行，则为 true；否则为假。