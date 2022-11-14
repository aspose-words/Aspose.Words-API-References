---
title: DataColumnCollection
second_title: Aspose.Words for Java API 参考
description: 表示 a 的对象集合。
type: docs
weight: 15
url: /zh/java/com.aspose.words.net.system.data/datacolumncollection/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Iterable
```
public class DataColumnCollection implements Iterable
```

代表一个集合[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象[DataTable](../../com.aspose.words.net.system.data/datatable).
## 方法

| 方法 | 描述 |
| --- | --- |
| [add(System.Data.DataColumn column)](#add-com.aspose.words.net.System.Data.DataColumn-) | 创建并添加指定的[DataColumn](../../com.aspose.words.net.system.data/datacolumn)反对[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection). |
| [add(String columnName)](#add-java.lang.String-) | 创建并添加一个[DataColumn](../../com.aspose.words.net.system.data/datacolumn)具有指定名称的对象[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection). |
| [add(String columnName, Class type)](#add-java.lang.String-java.lang.Class-) | 创建并添加一个[DataColumn](../../com.aspose.words.net.system.data/datacolumn)具有指定名称和类型的对象[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection). |
| [add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull)](#add-java.lang.String-java.lang.Class-int-boolean-boolean-) | 创建并添加一个[DataColumn](../../com.aspose.words.net.system.data/datacolumn)具有指定名称、类型和特定值的列集合。 |
| [clear()](#clear--) | 清除任何列的集合。 |
| [contains(String name)](#contains-java.lang.String-) | 检查集合是否包含具有指定名称的列。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 获取[DataColumn](../../com.aspose.words.net.system.data/datacolumn)来自指定索引处的集合。 |
| [get(String name)](#get-java.lang.String-) | 获取[DataColumn](../../com.aspose.words.net.system.data/datacolumn)从具有指定名称的集合中。 |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) |  |
| [hashCode()](#hashCode--) |  |
| [indexOf(System.Data.DataColumn column)](#indexOf-com.aspose.words.net.System.Data.DataColumn-) | 获取由名称指定的列的索引。 |
| [indexOf(String columnName)](#indexOf-java.lang.String-) | 获取具有特定名称的列的索引（名称不区分大小写）。 |
| [iterator()](#iterator--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(System.Data.DataColumn column)](#remove-com.aspose.words.net.System.Data.DataColumn-) | 删除指定的[DataColumn](../../com.aspose.words.net.system.data/datacolumn)集合中的对象。 |
| [remove(String name)](#remove-java.lang.String-) | 删除[DataColumn](../../com.aspose.words.net.system.data/datacolumn)集合中具有指定名称的对象。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(System.Data.DataColumn column) {#add-com.aspose.words.net.System.Data.DataColumn-}
```
public void add(System.Data.DataColumn column)
```


创建并添加指定的[DataColumn](../../com.aspose.words.net.system.data/datacolumn)反对[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | 这[DataColumn](../../com.aspose.words.net.system.data/datacolumn)添加。 |

### add(String columnName) {#add-java.lang.String-}
```
public void add(String columnName)
```


创建并添加一个[DataColumn](../../com.aspose.words.net.system.data/datacolumn)具有指定名称的对象[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| columnName | java.lang.String | 列的名称。 |

### add(String columnName, Class type) {#add-java.lang.String-java.lang.Class-}
```
public System.Data.DataColumn add(String columnName, Class type)
```


创建并添加一个[DataColumn](../../com.aspose.words.net.system.data/datacolumn)具有指定名称和类型的对象[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| columnName | java.lang.String | 这[DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn\#getColumnName--) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn\#setColumnName-java.lang.String-)在创建列时使用。 |
| type | java.lang.Class | 这[DataColumn.getDataType()](../../com.aspose.words.net.system.data/datacolumn\#getDataType--) / [DataColumn.setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn\#setDataType-java.lang.Class-)的新列。 |

**退货:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn) - 新创建的[DataColumn](../../com.aspose.words.net.system.data/datacolumn).
### add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull) {#add-java.lang.String-java.lang.Class-int-boolean-boolean-}
```
public System.Data.DataColumn add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull)
```


创建并添加一个[DataColumn](../../com.aspose.words.net.system.data/datacolumn)具有指定名称、类型和特定值的列集合。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| columnName | java.lang.String | 姓名 |
| type | java.lang.Class | 数据类型 |
| columnMapping | int | 列映射类型 |
| allowAutoIncrement | boolean | 是否允许自动递增 |
| allowDBNull | boolean | 是否允许 DBNull 值 |

**退货:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn) 创建了一个[DataColumn](../../com.aspose.words.net.system.data/datacolumn)实例。
### clear() {#clear--}
```
public void clear()
```


清除任何列的集合。

### contains(String name) {#contains-java.lang.String-}
```
public boolean contains(String name)
```


检查集合是否包含具有指定名称的列。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 这[DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn\#getColumnName--) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn\#setColumnName-java.lang.String-)要查找的列。 |

**退货:**
boolean - 如果存在具有此名称的列，则为 true；否则为假。
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
### get(int index) {#get-int-}
```
public System.Data.DataColumn get(int index)
```


获取[DataColumn](../../com.aspose.words.net.system.data/datacolumn)来自指定索引处的集合。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 要返回的列的从零开始的索引。 |

**退货:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn) - 这[DataColumn](../../com.aspose.words.net.system.data/datacolumn)在指定的索引处。
### get(String name) {#get-java.lang.String-}
```
public System.Data.DataColumn get(String name)
```


获取[DataColumn](../../com.aspose.words.net.system.data/datacolumn)从具有指定名称的集合中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 这[DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn\#getColumnName--) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn\#setColumnName-java.lang.String-)要返回的列。 |

**退货:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn) - 这[DataColumn](../../com.aspose.words.net.system.data/datacolumn)在具有指定的集合中[DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn\#getColumnName--) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn\#setColumnName-java.lang.String-);否则为空值，如果[DataColumn](../../com.aspose.words.net.system.data/datacolumn)不存在。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getCount() {#getCount--}
```
public int getCount()
```




**退货:**
int - 集合中的元素总数。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### indexOf(System.Data.DataColumn column) {#indexOf-com.aspose.words.net.System.Data.DataColumn-}
```
public int indexOf(System.Data.DataColumn column)
```


获取由名称指定的列的索引。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | 要返回的列的名称。 |

**退货:**
int - 如果找到，则为 column 指定的列的索引；否则，-1。
### indexOf(String columnName) {#indexOf-java.lang.String-}
```
public int indexOf(String columnName)
```


获取具有特定名称的列的索引（名称不区分大小写）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| columnName | java.lang.String | 要查找的列的名称。 |

**退货:**
int - 具有指定名称的列的从零开始的索引，如果该列在集合中不存在，则为 -1。
### iterator() {#iterator--}
```
public Iterator iterator()
```




**退货:**
java.util.Iterator
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### remove(System.Data.DataColumn column) {#remove-com.aspose.words.net.System.Data.DataColumn-}
```
public void remove(System.Data.DataColumn column)
```


删除指定的[DataColumn](../../com.aspose.words.net.system.data/datacolumn)集合中的对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | 这[DataColumn](../../com.aspose.words.net.system.data/datacolumn)去除。 |

### remove(String name) {#remove-java.lang.String-}
```
public void remove(String name)
```


删除[DataColumn](../../com.aspose.words.net.system.data/datacolumn)集合中具有指定名称的对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 要删除的列的名称。 |

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
