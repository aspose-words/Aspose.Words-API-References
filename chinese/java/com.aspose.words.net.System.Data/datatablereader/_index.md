---
title: DataTableReader
second_title: Aspose.Words for Java API 参考
description:以一个或多个只读只进结果集的形式获取一个或多个对象的内容。
type: docs
weight: 27
url: /zh/java/com.aspose.words.net.system.data/datatablereader/
---

**遗产:**
java.lang.Object, [com.aspose.words.net.System.Data.Common.DbDataReader](../../com.aspose.words.net.system.data.common/dbdatareader)
```
public class DataTableReader extends System.Data.Common.DbDataReader
```

这[DataTableReader](../../com.aspose.words.net.system.data/datatablereader)获取一个或多个的内容[DataTable](../../com.aspose.words.net.system.data/datatable)一个或多个只读、只进结果集形式的对象。
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [DataTableReader(System.Data.DataTable dataTable)](#DataTableReader-com.aspose.words.net.System.Data.DataTable-) | 初始化一个新的实例[DataTableReader](../../com.aspose.words.net.system.data/datatablereader)使用提供的数据进行分类[DataTable](../../com.aspose.words.net.system.data/datatable). |
| [DataTableReader(System.Data.DataTable[] dataTables)](#DataTableReader-com.aspose.words.net.System.Data.DataTable---) | 初始化一个新的实例[DataTableReader](../../com.aspose.words.net.system.data/datatablereader)类使用提供的数组[DataTable](../../com.aspose.words.net.system.data/datatable)对象。 |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [close()](#close--) | 关闭当前[DataTableReader](../../com.aspose.words.net.system.data/datatablereader). |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int ordinal)](#get-int-) | 在给定列序号的情况下，以其本机格式获取指定列的值。 |
| [get(String name)](#get-java.lang.String-) | 在给定列名的情况下，以本机格式获取指定列的值。 |
| [get班级()](#get班级--) |  |
| [getDepth()](#getDepth--) | 当前行的嵌套深度[DataTableReader](../../com.aspose.words.net.system.data/datatablereader). |
| [get字段Count()](#get字段Count--) | 返回当前行的列数。 |
| [get字段类型(int ordinal)](#get字段类型-int-) | 获取作为对象数据类型的 java.lang.班级。 |
| [getName(int ordinal)](#getName-int-) | 以 java.lang.String 形式获取指定列的值。 |
| [getRecordsAffected()](#getRecordsAffected--) | 获取通过执行 SQL 语句插入、更改或删除的行数。 |
| [getSchemaTable()](#getSchemaTable--) | 返回一个[DataTable](../../com.aspose.words.net.system.data/datatable)描述列元数据的[DataTableReader](../../com.aspose.words.net.system.data/datatablereader). |
| [getValue(int ordinal)](#getValue-int-) | 以本机格式获取指定列的值。 |
| [hasRows()](#hasRows--) | 获取一个值，该值指示是否[DataTableReader](../../com.aspose.words.net.system.data/datatablereader)包含一或多行。 |
| [hashCode()](#hashCode--) |  |
| [isClosed()](#isClosed--) | 获取一个值，该值指示是否[DataTableReader](../../com.aspose.words.net.system.data/datatablereader)已经关了。 |
| [iterator()](#iterator--) | 返回一个可用于遍历项目集合的枚举器。 |
| [nextResult()](#nextResult--) | 推进[DataTableReader](../../com.aspose.words.net.system.data/datatablereader)到下一个结果集，如果有的话。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [read()](#read--) | 推进[DataTableReader](../../com.aspose.words.net.system.data/datatablereader)到下一条记录。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DataTableReader(System.Data.DataTable dataTable) {#DataTableReader-com.aspose.words.net.System.Data.DataTable-}
```
public DataTableReader(System.Data.DataTable dataTable)
```


初始化一个新的实例[DataTableReader](../../com.aspose.words.net.system.data/datatablereader)使用提供的数据进行分类[DataTable](../../com.aspose.words.net.system.data/datatable).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable) | 这[DataTable](../../com.aspose.words.net.system.data/datatable)从哪个新[DataTableReader](../../com.aspose.words.net.system.data/datatablereader)获得其结果集。 |

### DataTableReader(System.Data.DataTable[] dataTables) {#DataTableReader-com.aspose.words.net.System.Data.DataTable---}
```
public DataTableReader(System.Data.DataTable[] dataTables)
```


初始化一个新的实例[DataTableReader](../../com.aspose.words.net.system.data/datatablereader)类使用提供的数组[DataTable](../../com.aspose.words.net.system.data/datatable)对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataTables | [DataTable\[\]](../../com.aspose.words.net.system.data/datatable) | 数组[DataTable](../../com.aspose.words.net.system.data/datatable)提供新结果的对象[DataTableReader](../../com.aspose.words.net.system.data/datatablereader)目的。 |

### close() {#close--}
```
public void close()
```


关闭当前[DataTableReader](../../com.aspose.words.net.system.data/datatablereader).

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### get(int ordinal) {#get-int-}
```
public Object get(int ordinal)
```


在给定列序号的情况下，以其本机格式获取指定列的值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ordinal | int | 从零开始的列序号。 |

**退货:**
java.lang.Object - 本机格式的指定列的值。
### get(String name) {#get-java.lang.String-}
```
public Object get(String name)
```


在给定列名的情况下，以本机格式获取指定列的值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 列的名称。 |

**退货:**
java.lang.Object - 本机格式的指定列的值。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getDepth() {#getDepth--}
```
public int getDepth()
```


当前行的嵌套深度[DataTableReader](../../com.aspose.words.net.system.data/datatablereader).

**退货:**
int - 当前行的嵌套深度；始终为零。
### get字段Count() {#get字段Count--}
```
public int get字段Count()
```


返回当前行的列数。

**退货:**
int - 未定位在有效结果集中时，为 0；否则为当前行的列数。
### get字段类型(int ordinal) {#get字段类型-int-}
```
public 班级 get字段类型(int ordinal)
```


获取作为对象数据类型的 java.lang.班级。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ordinal | int | 从零开始的列序号。 |

**退货:**
java.lang.班级 - 作为对象数据类型的 java.lang.班级。
### getName(int ordinal) {#getName-int-}
```
public String getName(int ordinal)
```


以 java.lang.String 形式获取指定列的值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ordinal | int | 从零开始的列序号 |

**退货:**
java.lang.String - 指定列的名称。
### getRecordsAffected() {#getRecordsAffected--}
```
public int getRecordsAffected()
```


获取通过执行 SQL 语句插入、更改或删除的行数。

**退货:**
诠释 - 的[DataTableReader](../../com.aspose.words.net.system.data/datatablereader)不支持此属性，始终返回 0。
### getSchemaTable() {#getSchemaTable--}
```
public System.Data.DataTable getSchemaTable()
```


返回一个[DataTable](../../com.aspose.words.net.system.data/datatable)描述列元数据的[DataTableReader](../../com.aspose.words.net.system.data/datatablereader).

**退货:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - 一个[DataTable](../../com.aspose.words.net.system.data/datatable)描述列元数据。
### getValue(int ordinal) {#getValue-int-}
```
public Object getValue(int ordinal)
```


以本机格式获取指定列的值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ordinal | int | 从零开始的列序号 |

**退货:**
java.lang.Object - 指定列的值。此方法为空列返回 DBNull。
### hasRows() {#hasRows--}
```
public boolean hasRows()
```


获取一个值，该值指示是否[DataTableReader](../../com.aspose.words.net.system.data/datatablereader)包含一或多行。

**退货:**
布尔值 - 如果[DataTableReader](../../com.aspose.words.net.system.data/datatablereader)包含一行或多行；否则为假。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isClosed() {#isClosed--}
```
public boolean isClosed()
```


获取一个值，该值指示是否[DataTableReader](../../com.aspose.words.net.system.data/datatablereader)已经关了。

**退货:**
 boolean - 如果[DataTableReader](../../com.aspose.words.net.system.data/datatablereader)已经关了;否则为假。
### iterator() {#iterator--}
```
public Iterator iterator()
```


返回一个可用于遍历项目集合的枚举器。

**退货:**
java.util.Iterator - 一个表示项目集合的 java.util.Iterator 对象。
### nextResult() {#nextResult--}
```
public boolean nextResult()
```


推进[DataTableReader](../../com.aspose.words.net.system.data/datatablereader)到下一个结果集，如果有的话。

**退货:**
boolean - 如果有另一个结果集，则为 true；否则为假。
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### read() {#read--}
```
public boolean read()
```


推进[DataTableReader](../../com.aspose.words.net.system.data/datatablereader)到下一条记录。

**退货:**
boolean - 如果还有另一行要读取，则为 true；否则为假。
### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
