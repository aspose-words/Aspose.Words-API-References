---
title: DataTableCollection
second_title: Aspose.Words for Java API 参考
description:表示 的表的集合。
type: docs
weight: 26
url: /zh/java/com.aspose.words.net.system.data/datatablecollection/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
java.lang.Iterable
```
public class DataTableCollection implements Iterable
```

表示表的集合[DataSet](../../com.aspose.words.net.system.data/dataset).
## 方法s

| 方法 | 描述 |
| --- | --- |
| [add(System.Data.DataTable table)](#add-com.aspose.words.net.System.Data.DataTable-) | 将指定的 DataTable 添加到集合中。 |
| [add(String name)](#add-java.lang.String-) | 创建一个[DataTable](../../com.aspose.words.net.system.data/datatable)使用指定的名称对象并将其添加到集合中。 |
| [contains(String name)](#contains-java.lang.String-) | 获取一个值，该值指示是否[DataTable](../../com.aspose.words.net.system.data/datatable)集合中存在具有指定名称的对象。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 获取[DataTable](../../com.aspose.words.net.system.data/datatable)指定索引处的对象。 |
| [get(String name)](#get-java.lang.String-) | 获取[DataTable](../../com.aspose.words.net.system.data/datatable)具有指定名称的对象。 |
| [get(String name, String tableNamespace)](#get-java.lang.String-java.lang.String-) | 获取[DataTable](../../com.aspose.words.net.system.data/datatable)指定命名空间中具有指定名称的对象。 |
| [get班级()](#get班级--) |  |
| [getCount()](#getCount--) |  |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(System.Data.DataTable table) {#add-com.aspose.words.net.System.Data.DataTable-}
```
public void add(System.Data.DataTable table)
```


将指定的 DataTable 添加到集合中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable) | 要添加的 DataTable 对象。 |

### add(String name) {#add-java.lang.String-}
```
public System.Data.DataTable add(String name)
```


创建一个[DataTable](../../com.aspose.words.net.system.data/datatable)使用指定的名称对象并将其添加到集合中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 给创建的名称[DataTable](../../com.aspose.words.net.system.data/datatable). |

**退货:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - 新创建的[DataTable](../../com.aspose.words.net.system.data/datatable).
### contains(String name) {#contains-java.lang.String-}
```
public boolean contains(String name)
```


获取一个值，该值指示是否[DataTable](../../com.aspose.words.net.system.data/datatable)集合中存在具有指定名称的对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 的名称[DataTable](../../com.aspose.words.net.system.data/datatable)找到。 |

**退货:**
boolean - 如果指定的表存在，则为 true；否则为假。
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
public System.Data.DataTable get(int index)
```


获取[DataTable](../../com.aspose.words.net.system.data/datatable)指定索引处的对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 从零开始的索引[DataTable](../../com.aspose.words.net.system.data/datatable)找到。 |

**退货:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - 一个[DataTable](../../com.aspose.words.net.system.data/datatable).
### get(String name) {#get-java.lang.String-}
```
public System.Data.DataTable get(String name)
```


获取[DataTable](../../com.aspose.words.net.system.data/datatable)具有指定名称的对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 要查找的 DataTable 的名称。 |

**退货:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - 一个[DataTable](../../com.aspose.words.net.system.data/datatable)具有指定名称；如果[DataTable](../../com.aspose.words.net.system.data/datatable)不存在。
### get(String name, String tableNamespace) {#get-java.lang.String-java.lang.String-}
```
public System.Data.DataTable get(String name, String tableNamespace)
```


获取[DataTable](../../com.aspose.words.net.system.data/datatable)指定命名空间中具有指定名称的对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 要查找的 DataTable 的名称。 |
| tableNamespace | java.lang.String | 的名称[DataTable](../../com.aspose.words.net.system.data/datatable)要查看的命名空间。 |

**退货:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - 一个[DataTable](../../com.aspose.words.net.system.data/datatable)具有指定名称；如果[DataTable](../../com.aspose.words.net.system.data/datatable)不存在。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getCount() {#getCount--}
```
public int getCount()
```




**退货:**
int - 此集合中的项目总数。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
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
