---
title: DataRelationCollection
second_title: Aspose.Words for Java API 参考
description:表示 this 的对象集合。
type: docs
weight: 19
url: /zh/java/com.aspose.words.net.system.data/datarelationcollection/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
java.lang.Iterable
```
public class DataRelationCollection implements Iterable
```

代表集合[DataRelation](../../com.aspose.words.net.system.data/datarelation)为此的对象[DataSet](../../com.aspose.words.net.system.data/dataset).
## 方法s

| 方法 | 描述 |
| --- | --- |
| [add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#add-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-) | 创建一个[DataRelation](../../com.aspose.words.net.system.data/datarelation)具有指定的父列和子列，并将其添加到集合中。 |
| [add(System.Data.DataRelation relation)](#add-com.aspose.words.net.System.Data.DataRelation-) | 添加一个[DataRelation](../../com.aspose.words.net.system.data/datarelation)到[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection). |
| [add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName)](#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String-java.lang.String-) | 向集合添加关系。 |
| [add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)](#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String---) | 向集合添加关系。 |
| [add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-) | 创建一个[DataRelation](../../com.aspose.words.net.system.data/datarelation)具有指定的名称、父列和子列，并将其添加到集合中。 |
| [add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)](#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean-) | 创建一个[DataRelation](../../com.aspose.words.net.system.data/datarelation)具有指定的名称、父列和子列，根据 createConstraints 参数的值具有可选约束，并将其添加到集合中。 |
| [clear()](#clear--) | 清除所有关系的集合。 |
| [contains(System.Data.DataRelation relation)](#contains-com.aspose.words.net.System.Data.DataRelation-) | 验证集合中是否存在具有特定名称（不区分大小写）的 DataRelation。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 获取[DataRelation](../../com.aspose.words.net.system.data/datarelation)指定索引处的对象。 |
| [get(String name)](#get-java.lang.String-) | 获取[DataRelation](../../com.aspose.words.net.system.data/datarelation)由名称指定的对象。 |
| [get班级()](#get班级--) |  |
| [getCount()](#getCount--) |  |
| [hashCode()](#hashCode--) |  |
| [indexOf(System.Data.DataRelation relation)](#indexOf-com.aspose.words.net.System.Data.DataRelation-) | 获取指定的索引[DataRelation](../../com.aspose.words.net.system.data/datarelation)目的。 |
| [iterator()](#iterator--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeAt(int index)](#removeAt-int-) | 从集合中删除指定索引处的关系。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#add-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-}
```
public void add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


创建一个[DataRelation](../../com.aspose.words.net.system.data/datarelation)具有指定的父列和子列，并将其添加到集合中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | 关系的父列。 |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | 关系的子列。 |

### add(System.Data.DataRelation relation) {#add-com.aspose.words.net.System.Data.DataRelation-}
```
public void add(System.Data.DataRelation relation)
```


添加一个[DataRelation](../../com.aspose.words.net.system.data/datarelation)到[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation) | 要添加到集合中的 DataRelation。 |

### add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName) {#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String-java.lang.String-}
```
public void add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName)
```


向集合添加关系。不检查重复等。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable) | 关系的父表。 |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable) | 关系的子表。 |
| parentColumnName | java.lang.String | 关系的父列的名称。 |
| childColumnName | java.lang.String | 关系的子列的名称。 |

### add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames) {#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String---}
```
public void add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)
```


向集合添加关系。不检查重复等。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable) | 关系的父表。 |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable) | 关系的子表。 |
| parentColumnNames | java.lang.String[] | 关系的父列名称数组。 |
| childColumnNames | java.lang.String[] | 关系的子列名称数组。 |

### add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-}
```
public void add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


创建一个[DataRelation](../../com.aspose.words.net.system.data/datarelation)具有指定的名称、父列和子列，并将其添加到集合中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 关系的名称。 |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | 关系的父列。 |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | 关系的子列。 |

### add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints) {#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean-}
```
public void add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)
```


创建一个[DataRelation](../../com.aspose.words.net.system.data/datarelation)具有指定的名称、父列和子列，根据 createConstraints 参数的值具有可选约束，并将其添加到集合中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 关系的名称。 |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | 关系的父列。 |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | 关系的子列。 |
| createConstraints | boolean | true 创建约束；否则为假。 （默认为真）。 |

### clear() {#clear--}
```
public void clear()
```


清除所有关系的集合。

### contains(System.Data.DataRelation relation) {#contains-com.aspose.words.net.System.Data.DataRelation-}
```
public boolean contains(System.Data.DataRelation relation)
```


验证集合中是否存在具有特定名称（不区分大小写）的 DataRelation。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation) | 要查找的关系的名称。 |

**退货:**
boolean - 如果存在具有指定名称的关系，则为 true；否则为假。
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
public System.Data.DataRelation get(int index)
```


获取[DataRelation](../../com.aspose.words.net.system.data/datarelation)指定索引处的对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 要查找的从零开始的索引。 |

**退货:**
[DataRelation](../../com.aspose.words.net.system.data/datarelation) - 这[DataRelation](../../com.aspose.words.net.system.data/datarelation) , 或者如果指定了 null 值[DataRelation](../../com.aspose.words.net.system.data/datarelation)不存在。
### get(String name) {#get-java.lang.String-}
```
public System.Data.DataRelation get(String name)
```


获取[DataRelation](../../com.aspose.words.net.system.data/datarelation)由名称指定的对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 要查找的关系的名称。 |

**退货:**
[DataRelation](../../com.aspose.words.net.system.data/datarelation) 被命名的[DataRelation](../../com.aspose.words.net.system.data/datarelation) , 或者如果指定了 null 值[DataRelation](../../com.aspose.words.net.system.data/datarelation)不存在。
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
int - 集合中的元素总数
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### indexOf(System.Data.DataRelation relation) {#indexOf-com.aspose.words.net.System.Data.DataRelation-}
```
public int indexOf(System.Data.DataRelation relation)
```


获取指定的索引[DataRelation](../../com.aspose.words.net.system.data/datarelation)目的。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation) | 要搜索的关系。 |

**退货:**
int - 关系的从 0 开始的索引，如果在集合中找不到关系，则为 -1。
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




### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


从集合中删除指定索引处的关系。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 要删除的关系的索引。 |

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
