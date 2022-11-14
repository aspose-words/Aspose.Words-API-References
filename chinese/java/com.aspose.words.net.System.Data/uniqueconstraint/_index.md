---
title: UniqueConstraint
second_title: Aspose.Words for Java API 参考
description: 表示对一组列的限制，其中所有值都必须是唯一的。
type: docs
weight: 32
url: /zh/java/com.aspose.words.net.system.data/uniqueconstraint/
---

**遗产:**
java.lang.Object, [com.aspose.words.net.System.Data.Constraint](../../com.aspose.words.net.system.data/constraint)
```
public class UniqueConstraint extends System.Data.Constraint
```

表示对一组列的限制，其中所有值都必须是唯一的。
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey)](#UniqueConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---boolean-) | 初始化一个新的实例[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint)具有指定名称的类，一个数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)要约束的对象，以及指定约束是否是主键的值。 |
| [UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---boolean-) | 初始化一个新的实例[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint)具有数组的类[DataColumn](../../com.aspose.words.net.system.data/datacolumn)要约束的对象，以及指定约束是否是主键的值。 |
| [UniqueConstraint(System.Data.DataColumn[] columns)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---) | 初始化一个新的实例[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint)具有给定数组的类[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象。 |
| [UniqueConstraint(System.Data.DataColumn column)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn-) | 初始化一个新的实例[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint)类与指定[DataColumn](../../com.aspose.words.net.system.data/datacolumn). |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object key2)](#equals-java.lang.Object-) | 将此约束与一秒进行比较以确定两者是否相同。 |
| [getClass()](#getClass--) |  |
| [getColumns()](#getColumns--) | 获取此约束影响的列数组。 |
| [getConstraintName()](#getConstraintName--) | 约束中的名称[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection). |
| [getTable()](#getTable--) | 获取此约束所属的表。 |
| [hashCode()](#hashCode--) |  |
| [isPrimaryKey()](#isPrimaryKey--) | 获取一个值，该值指示约束是否在主键上。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setConstraintName(String value)](#setConstraintName-java.lang.String-) | 约束中的名称[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection). |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey) {#UniqueConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---boolean-}
```
public UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey)
```


初始化一个新的实例[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint)具有指定名称的类，一个数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)要约束的对象，以及指定约束是否是主键的值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 约束的名称。 |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) | 一个数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)要约束的对象。 |
| isPrimaryKey | boolean | true 表示约束是主键；否则为假。 |

### UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---boolean-}
```
public UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey)
```


初始化一个新的实例[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint)具有数组的类[DataColumn](../../com.aspose.words.net.system.data/datacolumn)要约束的对象，以及指定约束是否是主键的值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) | 一个数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)要约束的对象。 |
| isPrimaryKey | boolean | true 表示约束是主键；否则为假。 |

### UniqueConstraint(System.Data.DataColumn[] columns) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---}
```
public UniqueConstraint(System.Data.DataColumn[] columns)
```


初始化一个新的实例[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint)具有给定数组的类[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) | 的数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)要约束的对象。 |

### UniqueConstraint(System.Data.DataColumn column) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn-}
```
public UniqueConstraint(System.Data.DataColumn column)
```


初始化一个新的实例[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint)类与指定[DataColumn](../../com.aspose.words.net.system.data/datacolumn).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | 这[DataColumn](../../com.aspose.words.net.system.data/datacolumn)来约束。 |

### equals(Object key2) {#equals-java.lang.Object-}
```
public boolean equals(Object key2)
```


将此约束与一秒进行比较以确定两者是否相同。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key2 | java.lang.Object | 这个对象[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint)进行比较。 |

**退货:**
boolean - 如果约束相等，则为 true；否则为假。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getColumns() {#getColumns--}
```
public System.Data.DataColumn[] getColumns()
```


获取此约束影响的列数组。

**退货:**
com.aspose.words.net.System.Data.DataColumn[ ] - 一个数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象。
### getConstraintName() {#getConstraintName--}
```
public String getConstraintName()
```


约束中的名称[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection).

**退货:**
java.lang.String - 的名称[Constraint](../../com.aspose.words.net.system.data/constraint).
### getTable() {#getTable--}
```
public System.Data.DataTable getTable()
```


获取此约束所属的表。

**退货:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - 这[DataTable](../../com.aspose.words.net.system.data/datatable)约束所属的。
### hashCode() {#hashCode--}
```
public int hashCode()
```




**退货:**
整数
### isPrimaryKey() {#isPrimaryKey--}
```
public boolean isPrimaryKey()
```


获取一个值，该值指示约束是否在主键上。

**退货:**
boolean - 如果约束在主键上，则为 true；否则为假。
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setConstraintName(String value) {#setConstraintName-java.lang.String-}
```
public void setConstraintName(String value)
```


约束中的名称[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 的名称[Constraint](../../com.aspose.words.net.system.data/constraint). |

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
