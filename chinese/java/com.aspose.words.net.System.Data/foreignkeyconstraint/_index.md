---
title: ForeignKeyConstraint
second_title: Aspose.Words for Java API 参考
description: 表示在删除或更新值或行时对主键/外键关系中的一组列实施的操作限制。
type: docs
weight: 29
url: /zh/java/com.aspose.words.net.system.data/foreignkeyconstraint/
---

**遗产：**
java.lang.Object, [com.aspose.words.net.System.Data.Constraint](../../com.aspose.words.net.system.data/constraint)
```
public class ForeignKeyConstraint extends System.Data.Constraint
```

表示在删除或更新值或行时对主键/外键关系中的一组列实施的操作限制。
## 构造器

| 构造函数 | 描述 |
| --- | --- |
| [ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns)](#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---) | 初始化一个新的实例[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint)具有指定名称的类，以及父子数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象。 |
| [ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#ForeignKeyConstraint-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-) | 初始化一个新的实例[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint)与指定的父母和孩子一起上课[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象。 |
| [ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-) | 初始化一个新的实例[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint)具有指定名称、父项和子项的类[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object key)](#equals-java.lang.Object-) | 获取一个值，该值指示当前是否[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint)与指定对象相同。 |
| [getClass()](#getClass--) |  |
| [getColumns()](#getColumns--) | 获取此约束的子列。 |
| [getConstraintName()](#getConstraintName--) | 约束中的名称[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection). |
| [getDeleteRule()](#getDeleteRule--) | 获取删除行时跨该约束发生的操作。 |
| [getRelatedColumns()](#getRelatedColumns--) | 此约束的父列。 |
| [getRelatedTable()](#getRelatedTable--) | 获取此约束的父表。 |
| [getTable()](#getTable--) | 获取此约束的子表。 |
| [getUpdateRule()](#getUpdateRule--) | 获取在更新行时跨越此约束发生的操作。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setConstraintName(String value)](#setConstraintName-java.lang.String-) | 约束中的名称[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection). |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns) {#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---}
```
public ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns)
```


初始化一个新的实例[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint)具有指定名称的类，以及父子数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| constraintName | java.lang.String | 的名称[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint).如果为 null 或空字符串，则在添加到约束集合时将给出默认名称。 |
| parentColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) | 父数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)在约束中。 |
| childColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) | 子数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)在约束中。 |

### ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#ForeignKeyConstraint-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-}
```
public ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


初始化一个新的实例[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint)与指定的父母和孩子一起上课[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | 父母[DataColumn](../../com.aspose.words.net.system.data/datacolumn)在约束中。 |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | 孩子[DataColumn](../../com.aspose.words.net.system.data/datacolumn)在约束中。 |

### ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-}
```
public ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


初始化一个新的实例[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint)具有指定名称、父项和子项的类[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| constraintName | java.lang.String | 约束的名称。 |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | 父母[DataColumn](../../com.aspose.words.net.system.data/datacolumn)在约束中。 |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | 孩子[DataColumn](../../com.aspose.words.net.system.data/datacolumn)在约束中。 |

### equals(Object key) {#equals-java.lang.Object-}
```
public boolean equals(Object key)
```


获取一个值，该值指示当前是否[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint)与指定对象相同。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | java.lang.Object | 这个对象[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint)被比较。二[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint)如果它们约束相同的列，则它们是相等的。 |

**退货：**
boolean - 如果对象相同，则为 true；否则，假的。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getColumns() {#getColumns--}
```
public System.Data.DataColumn[] getColumns()
```


获取此约束的子列。

**退货：**
com.aspose.words.net.System.Data.DataColumn[ ] - 一个数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)作为约束的子列的对象。
### getConstraintName() {#getConstraintName--}
```
public String getConstraintName()
```


约束中的名称[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection).

**退货：**
java.lang.String - 的名称[Constraint](../../com.aspose.words.net.system.data/constraint).
### getDeleteRule() {#getDeleteRule--}
```
public System.Data.Rule getDeleteRule()
```


获取删除行时跨该约束发生的操作。

**退货：**
[Rule](../../com.aspose.words.net.system.data/rule) - 中的一个[Rule](../../com.aspose.words.net.system.data/rule)价值观。默认值为级联。返回值是其中之一[Rule](../../com.aspose.words.net.system.data/rule)常数。
### getRelatedColumns() {#getRelatedColumns--}
```
public System.Data.DataColumn[] getRelatedColumns()
```


此约束的父列。

**退货：**
com.aspose.words.net.System.Data.DataColumn[ ] - 一个数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)作为约束的父列的对象。
### getRelatedTable() {#getRelatedTable--}
```
public System.Data.DataTable getRelatedTable()
```


获取此约束的父表。

**退货：**
[DataTable](../../com.aspose.words.net.system.data/datatable) - 父母[DataTable](../../com.aspose.words.net.system.data/datatable)的这个约束。
### getTable() {#getTable--}
```
public System.Data.DataTable getTable()
```


获取此约束的子表。

**退货：**
[DataTable](../../com.aspose.words.net.system.data/datatable) - 一个[DataTable](../../com.aspose.words.net.system.data/datatable)那是约束中的子表。
### getUpdateRule() {#getUpdateRule--}
```
public System.Data.Rule getUpdateRule()
```


获取在更新行时跨越此约束发生的操作。

**退货：**
[Rule](../../com.aspose.words.net.system.data/rule) - 中的一个[Rule](../../com.aspose.words.net.system.data/rule)价值观。默认值为级联。返回值是其中之一[Rule](../../com.aspose.words.net.system.data/rule)常数。
### hashCode() {#hashCode--}
```
public int hashCode()
```




**退货：**
整数
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

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 的名称[Constraint](../../com.aspose.words.net.system.data/constraint). |

### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
