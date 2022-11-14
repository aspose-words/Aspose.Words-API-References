---
title: DataRowCollection
second_title: Aspose.Words for Java API 参考
description: 表示 的行集合。
type: docs
weight: 21
url: /zh/java/com.aspose.words.net.system.data/datarowcollection/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Iterable
```
public class DataRowCollection implements Iterable
```

表示一个行的集合[DataTable](../../com.aspose.words.net.system.data/datatable).
## 方法

| 方法 | 描述 |
| --- | --- |
| [add(System.Data.DataRow row)](#add-com.aspose.words.net.System.Data.DataRow-) | 添加指定的[DataRow](../../com.aspose.words.net.system.data/datarow)到[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection)目的。 |
| [add(Object[] values)](#add-java.lang.Object...-) | 使用指定的值创建一行并将其添加到[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection). |
| [clear()](#clear--) | 清除所有行的集合。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [find(Object[] keys)](#find-java.lang.Object---) | 获取包含指定主键值的行。 |
| [find(String primaryKeyValue)](#find-java.lang.String-) | 获取由主键值指定的行。 |
| [get(int index)](#get-int-) | 获取指定索引处的行。 |
| [get(Object[] values)](#get-java.lang.Object---) | 获取包含指定值的行。 |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | 获取总数[DataRow](../../com.aspose.words.net.system.data/datarow)此集合中的对象。 |
| [hashCode()](#hashCode--) |  |
| [insertAt(System.Data.DataRow row, int pos)](#insertAt-com.aspose.words.net.System.Data.DataRow-int-) | 在集合中的指定位置插入一个新行。 |
| [iterator()](#iterator--) | 获取此集合的 java.util.Iterator。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeAt(int index)](#removeAt-int-) | 从集合中移除指定索引处的行。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(System.Data.DataRow row) {#add-com.aspose.words.net.System.Data.DataRow-}
```
public void add(System.Data.DataRow row)
```


添加指定的[DataRow](../../com.aspose.words.net.system.data/datarow)到[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection)目的。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow) | 这[DataRow](../../com.aspose.words.net.system.data/datarow)添加。 |

### add(Object[] values) {#add-java.lang.Object...-}
```
public void add(Object[] values)
```


使用指定的值创建一行并将其添加到[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| values | java.lang.Object[] | 用于创建新行的值数组。 |

### clear() {#clear--}
```
public void clear()
```


清除所有行的集合。

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
### find(Object[] keys) {#find-java.lang.Object---}
```
public System.Data.DataRow find(Object[] keys)
```


获取包含指定主键值的行。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| keys | java.lang.Object[] | 要查找的主键值数组。数组的类型是Object。 |

**退货:**
[DataRow](../../com.aspose.words.net.system.data/datarow) - 一个[DataRow](../../com.aspose.words.net.system.data/datarow)包含指定主键值的对象；否则如果主键值不存在则为空值[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection).
### find(String primaryKeyValue) {#find-java.lang.String-}
```
public System.Data.DataRow find(String primaryKeyValue)
```


获取由主键值指定的行。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| primaryKeyValue | java.lang.String | 要查找的 DataRow 的主键值。 |

**退货:**
[DataRow](../../com.aspose.words.net.system.data/datarow) - 包含指定主键值的 DataRow；如果 DataRowCollection 中不存在主键值，则为空值。
### get(int index) {#get-int-}
```
public System.Data.DataRow get(int index)
```


获取指定索引处的行。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 要返回的行的从零开始的索引。 |

**退货:**
[DataRow](../../com.aspose.words.net.system.data/datarow) - 指定的[DataRow](../../com.aspose.words.net.system.data/datarow).
### get(Object[] values) {#get-java.lang.Object---}
```
public System.Data.DataRow get(Object[] values)
```


获取包含指定值的行。如果存在主键的列，则将使用索引。如果没有索引，则使用简单的线性扫描。请小心处理，因为这可能会花费大量时间。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| values | java.lang.Object[] | 行的数据 |

**退货:**
[DataRow](../../com.aspose.words.net.system.data/datarow) 找到行或`null`
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


获取总数[DataRow](../../com.aspose.words.net.system.data/datarow)此集合中的对象。

**退货:**
int - 总数[DataRow](../../com.aspose.words.net.system.data/datarow)此集合中的对象。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### insertAt(System.Data.DataRow row, int pos) {#insertAt-com.aspose.words.net.System.Data.DataRow-int-}
```
public void insertAt(System.Data.DataRow row, int pos)
```


在集合中的指定位置插入一个新行。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow) | 这[DataRow](../../com.aspose.words.net.system.data/datarow)添加。 |
| pos | int | 集合中要添加 DataRow 的位置（从零开始）。 |

### iterator() {#iterator--}
```
public Iterator iterator()
```


获取此集合的 java.util.Iterator。

**退货:**
java.util.Iterator - 此集合的 java.util.Iterator。
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


从集合中移除指定索引处的行。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 要删除的行的索引。 |

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
