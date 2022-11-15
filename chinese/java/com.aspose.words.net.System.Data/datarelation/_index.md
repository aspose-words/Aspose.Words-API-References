---
title: DataRelation
second_title: Aspose.Words for Java API 参考
description: 表示两个对象之间的父/子关系。
type: docs
weight: 18
url: /zh/java/com.aspose.words.net.system.data/datarelation/
---

**遗产：**
java.lang.Object
```
public class DataRelation
```

表示两个之间的父/子关系[DataTable](../../com.aspose.words.net.system.data/datatable)对象。
## 构造器

| 构造函数 | 描述 |
| --- | --- |
| [DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String---) | 初始化一个新的实例[DataRelation](../../com.aspose.words.net.system.data/datarelation)使用指定名称的类、父表和子表、父列和子列的匹配数组。 |
| [DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---boolean-) | 初始化一个新的实例[DataRelation](../../com.aspose.words.net.system.data/datarelation)使用指定名称的类，匹配的父子数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象和指示是否创建约束的值。 |
| [DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean-) | 初始化一个新的实例[DataRelation](../../com.aspose.words.net.system.data/datarelation)使用指定名称、父级和子级的类[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象，以及指示是否创建约束的值。 |
| [DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-) | 初始化一个新的实例[DataRelation](../../com.aspose.words.net.system.data/datarelation)使用指定的类[DataRelation](../../com.aspose.words.net.system.data/datarelation)姓名，父母和孩子[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object-) |  |
| [getChildColumnNames()](#getChildColumnNames--) |  |
| [getChildColumns()](#getChildColumns--) | 得到孩子[DataColumn](../../com.aspose.words.net.system.data/datacolumn)这种关系的对象。 |
| [getChildKey()](#getChildKey--) |  |
| [getChildKeyConstraint()](#getChildKeyConstraint--) | 获取[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint)为关系。 |
| [getChildTable()](#getChildTable--) | 获取此关系的子表。 |
| [getChildTableName()](#getChildTableName--) |  |
| [getClass()](#getClass--) |  |
| [getDataSet()](#getDataSet--) | 获取[DataSet](../../com.aspose.words.net.system.data/dataset)到哪个[DataRelation](../../com.aspose.words.net.system.data/datarelation)属于。 |
| [getParentColumnNames()](#getParentColumnNames--) |  |
| [getParentColumns()](#getParentColumns--) | 获取一个数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)作为此父列的对象[DataRelation](../../com.aspose.words.net.system.data/datarelation). |
| [getParentKey()](#getParentKey--) |  |
| [getParentKeyConstraint()](#getParentKeyConstraint--) | 获取[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint)保证 a 的父列中的值[DataRelation](../../com.aspose.words.net.system.data/datarelation)是独一无二的。 |
| [getParentTable()](#getParentTable--) | 获取父级[DataTable](../../com.aspose.words.net.system.data/datatable)这个的[DataRelation](../../com.aspose.words.net.system.data/datarelation). |
| [getParentTableName()](#getParentTableName--) |  |
| [getRelationName()](#getRelationName--) | 获取用于检索的名称[DataRelation](../../com.aspose.words.net.system.data/datarelation)来自[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection). |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint)](#setChildKeyConstraint-com.aspose.words.net.System.Data.ForeignKeyConstraint-) |  |
| [setNested(boolean value)](#setNested-boolean-) | 设置一个值，指示是否[DataRelation](../../com.aspose.words.net.system.data/datarelation)对象是嵌套的。 |
| [setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint)](#setParentKeyConstraint-com.aspose.words.net.System.Data.UniqueConstraint-) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String---}
```
public DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)
```


初始化一个新的实例[DataRelation](../../com.aspose.words.net.system.data/datarelation)使用指定名称的类、父表和子表、父列和子列的匹配数组。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| relationName | java.lang.String | DataRelation 的名称。如果为 null 或空字符串 ("")，则在将创建的对象添加到 DataRelationCollection 时将给出一个默认名称。 |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable) | 关系中的父表。 |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable) | 关系中的子表。 |
| parentColumnNames | java.lang.String[] | 关系中父 DataColumn 的名称。 |
| childColumnNames | java.lang.String[] | 关系中的子 DataColumn；s。 |

### DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---boolean-}
```
public DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints)
```


初始化一个新的实例[DataRelation](../../com.aspose.words.net.system.data/datarelation)使用指定名称的类，匹配的父子数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象和指示是否创建约束的值。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| relationName | java.lang.String | 关系的名称。如果为 null 或空字符串 ("")，则在将创建的对象添加到[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection). |
| parentColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) | 父数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象。 |
| childColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) | 子数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象。 |
| createConstraints | boolean | 指示是否创建约束的值。如果创建了约束，则为 true。否则为假。 |

### DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean-}
```
public DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)
```


初始化一个新的实例[DataRelation](../../com.aspose.words.net.system.data/datarelation)使用指定名称、父级和子级的类[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象，以及指示是否创建约束的值。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| relationName | java.lang.String | 关系的名称。如果为 null 或空字符串 ("")，则在将创建的对象添加到[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection). |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | 父母[DataColumn](../../com.aspose.words.net.system.data/datacolumn)在关系中。 |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | 孩子[DataColumn](../../com.aspose.words.net.system.data/datacolumn)在关系中。 |
| createConstraints | boolean | 指示是否创建约束的值。如果创建了约束，则为 true。否则为假。 |

### DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-}
```
public DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


初始化一个新的实例[DataRelation](../../com.aspose.words.net.system.data/datarelation)使用指定的类[DataRelation](../../com.aspose.words.net.system.data/datarelation)姓名，父母和孩子[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| relationName | java.lang.String | 的名称[DataRelation](../../com.aspose.words.net.system.data/datarelation) .如果为 null 或空字符串 ("")，则在将创建的对象添加到[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection). |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | 父母[DataColumn](../../com.aspose.words.net.system.data/datacolumn)在关系中。 |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | 孩子[DataColumn](../../com.aspose.words.net.system.data/datacolumn)在关系中。 |

### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| obj | java.lang.Object |  |

**退货：**
布尔值
### getChildColumnNames() {#getChildColumnNames--}
```
public String[] getChildColumnNames()
```




**退货：**
java.lang.字符串[] - 此关系的子 DataColumn 名称。
### getChildColumns() {#getChildColumns--}
```
public System.Data.DataColumn[] getChildColumns()
```


得到孩子[DataColumn](../../com.aspose.words.net.system.data/datacolumn)这种关系的对象。

**退货：**
com.aspose.words.net.System.Data.DataColumn[ ] - 一个数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象。
### getChildKey() {#getChildKey--}
```
public System.Data.DataKey getChildKey()
```




**退货：**
[DataKey](../../com.aspose.words.net.system.data/datakey)
### getChildKeyConstraint() {#getChildKeyConstraint--}
```
public System.Data.ForeignKeyConstraint getChildKeyConstraint()
```


获取[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint)为关系。

**退货：**
[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) - 一个[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint).
### getChildTable() {#getChildTable--}
```
public System.Data.DataTable getChildTable()
```


获取此关系的子表。

**退货：**
[DataTable](../../com.aspose.words.net.system.data/datatable) - 一个[DataTable](../../com.aspose.words.net.system.data/datatable)那是关系的子表。
### getChildTableName() {#getChildTableName--}
```
public String getChildTableName()
```




**退货：**
java.lang.String - 此 DataRelation 的子 DataTable 的名称。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getDataSet() {#getDataSet--}
```
public System.Data.DataSet getDataSet()
```


获取[DataSet](../../com.aspose.words.net.system.data/dataset)到哪个[DataRelation](../../com.aspose.words.net.system.data/datarelation)属于。

**退货：**
[DataSet](../../com.aspose.words.net.system.data/dataset) - 一个[DataSet](../../com.aspose.words.net.system.data/dataset)到哪个[DataRelation](../../com.aspose.words.net.system.data/datarelation)属于。
### getParentColumnNames() {#getParentColumnNames--}
```
public String[] getParentColumnNames()
```




**退货：**
java.lang.字符串[] - 此关系的父 DataColumn 名称。
### getParentColumns() {#getParentColumns--}
```
public System.Data.DataColumn[] getParentColumns()
```


获取一个数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)作为此父列的对象[DataRelation](../../com.aspose.words.net.system.data/datarelation).

**退货：**
com.aspose.words.net.System.Data.DataColumn[ ] - 一个数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)作为此父列的对象[DataRelation](../../com.aspose.words.net.system.data/datarelation).
### getParentKey() {#getParentKey--}
```
public System.Data.DataKey getParentKey()
```




**退货：**
[DataKey](../../com.aspose.words.net.system.data/datakey)
### getParentKeyConstraint() {#getParentKeyConstraint--}
```
public System.Data.UniqueConstraint getParentKeyConstraint()
```


获取[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint)保证 a 的父列中的值[DataRelation](../../com.aspose.words.net.system.data/datarelation)是独一无二的。

**退货：**
[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) - 一个[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint)确保父列中的值是唯一的。
### getParentTable() {#getParentTable--}
```
public System.Data.DataTable getParentTable()
```


获取父级[DataTable](../../com.aspose.words.net.system.data/datatable)这个的[DataRelation](../../com.aspose.words.net.system.data/datarelation).

**退货：**
[DataTable](../../com.aspose.words.net.system.data/datatable) - 一个[DataTable](../../com.aspose.words.net.system.data/datatable)那是这个关系的父表。
### getParentTableName() {#getParentTableName--}
```
public String getParentTableName()
```




**退货：**
java.lang.String - 此 DataRelation 的父 DataTable 的名称。
### getRelationName() {#getRelationName--}
```
public String getRelationName()
```


获取用于检索的名称[DataRelation](../../com.aspose.words.net.system.data/datarelation)来自[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection).

**退货：**
 java.lang.String - a 的名称[DataRelation](../../com.aspose.words.net.system.data/datarelation).
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




### setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint) {#setChildKeyConstraint-com.aspose.words.net.System.Data.ForeignKeyConstraint-}
```
public void setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| childKeyConstraint | [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) |  |

### setNested(boolean value) {#setNested-boolean-}
```
public void setNested(boolean value)
```


设置一个值，指示是否[DataRelation](../../com.aspose.words.net.system.data/datarelation)对象是嵌套的。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 真的，如果[DataRelation](../../com.aspose.words.net.system.data/datarelation)对象是嵌套的；否则，假的。 |

### setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint) {#setParentKeyConstraint-com.aspose.words.net.System.Data.UniqueConstraint-}
```
public void setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| parentKeyConstraint | [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) |  |

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
