---
title: DataRow
second_title: Aspose.Words for Java API Reference
description: 表示 a 中的一行数据。
type: docs
weight: 20
url: /zh/java/com.aspose.words.net.system.data/datarow/
---

**遗产:**
java.lang.Object
```
public class DataRow
```

表示a中的一行数据[DataTable](../../com.aspose.words.net.system.data/datatable).
## 方法

| 方法 | 描述 |
| --- | --- |
| [delete()](#delete--) | 删除[DataRow](../../com.aspose.words.net.system.data/datarow). |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(System.Data.DataColumn column)](#get-com.aspose.words.net.System.Data.DataColumn-) | 获取存储在指定的数据[DataColumn](../../com.aspose.words.net.system.data/datacolumn). |
| [get(int columnIndex)](#get-int-) | 获取存储在索引指定的列中的数据。 |
| [get(String columnName)](#get-java.lang.String-) | 获取存储在 name 指定的列中的数据。 |
| [getChildRows(System.Data.DataRelation relation)](#getChildRows-com.aspose.words.net.System.Data.DataRelation-) | 获取 this 的子行[DataRow](../../com.aspose.words.net.system.data/datarow)使用指定的[DataRelation](../../com.aspose.words.net.system.data/datarelation). |
| [get班级()](#get班级--) |  |
| [getItemArray()](#getItemArray--) | 通过数组获取该行的所有值。 |
| [getKeyValues(System.Data.DataKey childKey)](#getKeyValues-com.aspose.words.net.System.Data.DataKey-) |  |
| [getOriginalValue(String columnName)](#getOriginalValue-java.lang.String-) |  |
| [getParentRow(System.Data.DataRelation relation)](#getParentRow-com.aspose.words.net.System.Data.DataRelation-) | 获取 a 的父行[DataRow](../../com.aspose.words.net.system.data/datarow)使用指定的[DataRelation](../../com.aspose.words.net.system.data/datarelation). |
| [getParentRows(System.Data.DataRelation relation)](#getParentRows-com.aspose.words.net.System.Data.DataRelation-) | 获取 a 的父行[DataRow](../../com.aspose.words.net.system.data/datarow)使用指定的[DataRelation](../../com.aspose.words.net.system.data/datarelation). |
| [getRowState()](#getRowState--) | 获取行的当前状态与它的关系[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection). |
| [getTable()](#getTable--) | 获取[DataTable](../../com.aspose.words.net.system.data/datatable)此行有一个架构。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [readFrom(ResultSet resultSet)](#readFrom-java.sql.ResultSet-) | 从 java.sql.ResultSet 中读取值 |
| [remove(int index)](#remove-int-) |  |
| [set(System.Data.DataColumn value, Object column)](#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object-) | 设置存储在指定的数据[DataColumn](../../com.aspose.words.net.system.data/datacolumn). |
| [set(int value, Object columnIndex)](#set-int-java.lang.Object-) | 设置存储在索引指定的列中的数据。 |
| [set(String value, Object columnName)](#set-java.lang.String-java.lang.Object-) | 设置存储在由名称指定的列中的数据。 |
| [setItemArray(Object[] value)](#setItemArray-java.lang.Object---) | 通过数组设置该行的所有值。 |
| [setOriginalValue(String columnName, Object data)](#setOriginalValue-java.lang.String-java.lang.Object-) |  |
| [setRowState(int state)](#setRowState-int-) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### delete() {#delete--}
```
public void delete()
```


删除[DataRow](../../com.aspose.words.net.system.data/datarow).

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
### get(System.Data.DataColumn column) {#get-com.aspose.words.net.System.Data.DataColumn-}
```
public Object get(System.Data.DataColumn column)
```


获取存储在指定的数据[DataColumn](../../com.aspose.words.net.system.data/datacolumn).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | 一个[DataColumn](../../com.aspose.words.net.system.data/datacolumn)包含数据。 |

**退货:**
java.lang.Object - 包含数据的 java.lang.Object。
### get(int columnIndex) {#get-int-}
```
public Object get(int columnIndex)
```


获取存储在索引指定的列中的数据。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| columnIndex | int | 列的从零开始的索引。 |

**退货:**
java.lang.Object - 包含数据的 java.lang.Object。
### get(String columnName) {#get-java.lang.String-}
```
public Object get(String columnName)
```


获取存储在 name 指定的列中的数据。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| columnName | java.lang.String | 列的名称。 |

**退货:**
java.lang.Object - 包含数据的 java.lang.Object。
### getChildRows(System.Data.DataRelation relation) {#getChildRows-com.aspose.words.net.System.Data.DataRelation-}
```
public System.Data.DataRow[] getChildRows(System.Data.DataRelation relation)
```


获取 this 的子行[DataRow](../../com.aspose.words.net.system.data/datarow)使用指定的[DataRelation](../../com.aspose.words.net.system.data/datarelation).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation) | 这[DataRelation](../../com.aspose.words.net.system.data/datarelation)使用。 |

**退货:**
com.aspose.words.net.System.Data.DataRow[ ] - 一个数组[DataRow](../../com.aspose.words.net.system.data/datarow)对象或长度为零的数组。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getItemArray() {#getItemArray--}
```
public Object[] getItemArray()
```


通过数组获取该行的所有值。

**退货:**
java.lang.Object[- java.lang.Object 类型的数组。
### getKeyValues(System.Data.DataKey childKey) {#getKeyValues-com.aspose.words.net.System.Data.DataKey-}
```
public Object[] getKeyValues(System.Data.DataKey childKey)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| childKey | [DataKey](../../com.aspose.words.net.system.data/datakey) |  |

**退货:**
java.lang.Object[]
### getOriginalValue(String columnName) {#getOriginalValue-java.lang.String-}
```
public Object getOriginalValue(String columnName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| columnName | java.lang.String |  |

**退货:**
java.lang.Object
### getParentRow(System.Data.DataRelation relation) {#getParentRow-com.aspose.words.net.System.Data.DataRelation-}
```
public System.Data.DataRow getParentRow(System.Data.DataRelation relation)
```


获取 a 的父行[DataRow](../../com.aspose.words.net.system.data/datarow)使用指定的[DataRelation](../../com.aspose.words.net.system.data/datarelation).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation) | 这[DataRelation](../../com.aspose.words.net.system.data/datarelation)使用。 |

**退货:**
[DataRow](../../com.aspose.words.net.system.data/datarow) - 父母[DataRow](../../com.aspose.words.net.system.data/datarow)当前行的。
### getParentRows(System.Data.DataRelation relation) {#getParentRows-com.aspose.words.net.System.Data.DataRelation-}
```
public System.Data.DataRow[] getParentRows(System.Data.DataRelation relation)
```


获取 a 的父行[DataRow](../../com.aspose.words.net.system.data/datarow)使用指定的[DataRelation](../../com.aspose.words.net.system.data/datarelation).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation) | 这[DataRelation](../../com.aspose.words.net.system.data/datarelation)使用。 |

**退货:**
com.aspose.words.net.System.Data.DataRow[ ] - 一个数组[DataRow](../../com.aspose.words.net.system.data/datarow)对象或长度为零的数组。
### getRowState() {#getRowState--}
```
public int getRowState()
```


获取行的当前状态与它的关系[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection).

**退货:**
int - 其中之一[DataRowState](../../com.aspose.words.net.system.data/datarowstate)价值观。返回值是按位组合[DataRowState](../../com.aspose.words.net.system.data/datarowstate)常数。
### getTable() {#getTable--}
```
public System.Data.DataTable getTable()
```


获取[DataTable](../../com.aspose.words.net.system.data/datatable)此行有一个架构。

**退货:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - 这[DataTable](../../com.aspose.words.net.system.data/datatable)该行所属的。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### readFrom(ResultSet resultSet) {#readFrom-java.sql.ResultSet-}
```
public boolean readFrom(ResultSet resultSet)
```


从 java.sql.ResultSet 中读取值

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | 要读取的存储 |

**退货:**
boolean - 如果没有发生读取错误，则为 true
### remove(int index) {#remove-int-}
```
public void remove(int index)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int |  |

### set(System.Data.DataColumn value, Object column) {#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object-}
```
public void set(System.Data.DataColumn value, Object column)
```


设置存储在指定的数据[DataColumn](../../com.aspose.words.net.system.data/datacolumn).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | 包含数据的 java.lang.Object。 |
| column | java.lang.Object | 一个[DataColumn](../../com.aspose.words.net.system.data/datacolumn)包含数据。 |

### set(int value, Object columnIndex) {#set-int-java.lang.Object-}
```
public void set(int value, Object columnIndex)
```


设置存储在索引指定的列中的数据。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 包含数据的 java.lang.Object。 |
| columnIndex | java.lang.Object | 列的从零开始的索引。 |

### set(String value, Object columnName) {#set-java.lang.String-java.lang.Object-}
```
public void set(String value, Object columnName)
```


设置存储在由名称指定的列中的数据。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 包含数据的 java.lang.Object。 |
| columnName | java.lang.Object | 列的名称。 |

### setItemArray(Object[] value) {#setItemArray-java.lang.Object---}
```
public void setItemArray(Object[] value)
```


通过数组设置该行的所有值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.Object[] | java.lang.Object 类型的数组。 |

### setOriginalValue(String columnName, Object data) {#setOriginalValue-java.lang.String-java.lang.Object-}
```
public void setOriginalValue(String columnName, Object data)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| columnName | java.lang.String |  |
| data | java.lang.Object |  |

### setRowState(int state) {#setRowState-int-}
```
public void setRowState(int state)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| state | int |  |

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
