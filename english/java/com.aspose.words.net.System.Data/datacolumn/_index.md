---
title: DataColumn
second_title: Aspose.Words for Java API Reference
description: 表示 a 中列的架构。
type: docs
weight: 14
url: /zh/java/com.aspose.words.net.system.data/datacolumn/
---

**遗产:**
java.lang.Object
```
public class DataColumn
```

表示 a 中列的架构[DataTable](../../com.aspose.words.net.system.data/datatable).
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [DataColumn()](#DataColumn--) | 初始化 a 的新实例[DataColumn](../../com.aspose.words.net.system.data/datacolumn)类作为类型字符串。 |
| [DataColumn(String columnName)](#DataColumn-java.lang.String-) | 初始化一个新的实例[DataColumn](../../com.aspose.words.net.system.data/datacolumn)类，作为类型字符串，使用指定的列名。 |
| [DataColumn(String name, System.Data.DataTable table)](#DataColumn-java.lang.String-com.aspose.words.net.System.Data.DataTable-) | 初始化 @ 的新实例\{链接数据列\使用指定的列名和它所属的表的类。 |
| [DataColumn(String columnName, 班级 data类型)](#DataColumn-java.lang.String-java.lang.班级-) | 初始化一个新的实例[DataColumn](../../com.aspose.words.net.system.data/datacolumn)类使用指定的列名和数据类型。 |
| [DataColumn(String name, 班级 type, System.Data.DataTable table)](#DataColumn-java.lang.String-java.lang.班级-com.aspose.words.net.System.Data.DataTable-) | 初始化一个新的实例[DataColumn](../../com.aspose.words.net.system.data/datacolumn)类使用指定的列名、数据类型和它所属的数据表。 |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet)](#areColumnSetsTheSame-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---) |  |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAllowDBNull()](#getAllowDBNull--) | 获取一个值，该值指示此列中是否允许属于该表的行的空值。 |
| [getAutoIncrement()](#getAutoIncrement--) | 获取一个值，该值指示该列是否为添加到表中的新行自动增加该列的值。 |
| [getAutoIncrementSeed()](#getAutoIncrementSeed--) | 获取具有它的列的起始值[getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn\#getAutoIncrement--) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn\#setAutoIncrement-boolean-)属性设置为真。 |
| [getAutoIncrementStep()](#getAutoIncrementStep--) | 获取列使用的增量及其[getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn\#getAutoIncrement--) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn\#setAutoIncrement-boolean-)属性设置为真。 |
| [getCaption()](#getCaption--) | 获取列的标题。 |
| [get班级()](#get班级--) |  |
| [getColumnMapping()](#getColumnMapping--) | 获取[Mapping类型](../../com.aspose.words.net.system.data/mappingtype)的列。 |
| [getColumnName()](#getColumnName--) | 获取列中的名称[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection). |
| [getData类型()](#getData类型--) | 获取存储在列中的数据类型。 |
| [getDefaultValue()](#getDefaultValue--) | 创建新行时获取列的默认值。 |
| [getExpression()](#getExpression--) | 获取用于筛选行、计算列中的值或创建聚合列的表达式。 |
| [getMaxLength()](#getMaxLength--) | 获取文本列的最大长度。 |
| [getNamespace()](#getNamespace--) | 获取命名空间[DataColumn](../../com.aspose.words.net.system.data/datacolumn). |
| [getOrdinal()](#getOrdinal--) | 获取列在[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection)收藏。 |
| [getPrefix()](#getPrefix--) | 获取一个 XML 前缀，该前缀为[DataTable](../../com.aspose.words.net.system.data/datatable). |
| [getReadOnly()](#getReadOnly--) | 获取一个值，该值指示列是否允许在将行添加到表后立即进行更改。 |
| [getTable()](#getTable--) | 获取[DataTable](../../com.aspose.words.net.system.data/datatable)该列所属的列。 |
| [getUnique()](#getUnique--) | 获取一个值，该值指示列的每一行中的值是否必须唯一。 |
| [hashCode()](#hashCode--) |  |
| [isReadOnly()](#isReadOnly--) |  |
| [isUnique()](#isUnique--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAllowDBNull(boolean value)](#setAllowDBNull-boolean-) | 设置一个值，该值指示此列中是否允许属于该表的行的空值。 |
| [setAutoIncrement(boolean value)](#setAutoIncrement-boolean-) | 设置一个值，该值指示列是否为添加到表中的新行自动增加列的值。 |
| [setAutoIncrementSeed(long value)](#setAutoIncrementSeed-long-) | 设置具有它的列的起始值[getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn\#getAutoIncrement--) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn\#setAutoIncrement-boolean-)属性设置为真。 |
| [setAutoIncrementStep(long value)](#setAutoIncrementStep-long-) | 设置列使用的增量及其[getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn\#getAutoIncrement--) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn\#setAutoIncrement-boolean-)属性设置为真。 |
| [setCaption(String value)](#setCaption-java.lang.String-) | 设置列的标题。 |
| [setColumnMapping(int value)](#setColumnMapping-int-) | 设置[Mapping类型](../../com.aspose.words.net.system.data/mappingtype)的列。 |
| [setColumnName(String value)](#setColumnName-java.lang.String-) | 设置列的名称[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection). |
| [setData类型(班级 value)](#setData类型-java.lang.班级-) | 设置存储在列中的数据类型。 |
| [setDefaultValue(Object value)](#setDefaultValue-java.lang.Object-) | 创建新行时设置列的默认值。 |
| [setMaxLength(int value)](#setMaxLength-int-) | 设置文本列的最大长度。 |
| [setNamespace(String value)](#setNamespace-java.lang.String-) | 设置命名空间[DataColumn](../../com.aspose.words.net.system.data/datacolumn). |
| [setOrdinal(int ordinal)](#setOrdinal-int-) | 改变序数或位置[DataColumn](../../com.aspose.words.net.system.data/datacolumn)到指定的序数或位置。 |
| [setPrefix(String value)](#setPrefix-java.lang.String-) | 设置一个 XML 前缀，为[DataTable](../../com.aspose.words.net.system.data/datatable). |
| [setReadOnly(boolean value)](#setReadOnly-boolean-) | 设置一个值，该值指示列是否允许在将行添加到表后立即进行更改。 |
| [setUnique(boolean value)](#setUnique-boolean-) | 设置一个值，该值指示列的每一行中的值是否必须唯一。 |
| [toString()](#toString--) | 获取[getExpression()](../../com.aspose.words.net.system.data/datacolumn\#getExpression--)列的，如果存在的话。 |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DataColumn() {#DataColumn--}
```
public DataColumn()
```


初始化 a 的新实例[DataColumn](../../com.aspose.words.net.system.data/datacolumn)类作为类型字符串。

### DataColumn(String columnName) {#DataColumn-java.lang.String-}
```
public DataColumn(String columnName)
```


初始化一个新的实例[DataColumn](../../com.aspose.words.net.system.data/datacolumn)类，作为类型字符串，使用指定的列名。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| columnName | java.lang.String | 一个字符串，表示要创建的列的名称。如果设置为 null 或空字符串 ("")，则在添加到列集合时将指定默认名称。 |

### DataColumn(String name, System.Data.DataTable table) {#DataColumn-java.lang.String-com.aspose.words.net.System.Data.DataTable-}
```
public DataColumn(String name, System.Data.DataTable table)
```


初始化 @ 的新实例\{链接数据列\使用指定的列名和它所属的表的类。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 数据列的名称 |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable) | 此列所属的表 |

### DataColumn(String columnName, 班级 data类型) {#DataColumn-java.lang.String-java.lang.班级-}
```
public DataColumn(String columnName, 班级 data类型)
```


初始化一个新的实例[DataColumn](../../com.aspose.words.net.system.data/datacolumn)类使用指定的列名和数据类型。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| columnName | java.lang.String | 一个字符串，表示要创建的列的名称。如果设置为 null 或空字符串 ("")，则在添加到列集合时将指定默认名称。 |
| data类型 | java.lang.班级 | 支持的[getData类型()](../../com.aspose.words.net.system.data/datacolumn\#getData类型--) / [setData类型(java.lang.班级)](../../com.aspose.words.net.system.data/datacolumn\#setData类型-java.lang.班级-). |

### DataColumn(String name, 班级 type, System.Data.DataTable table) {#DataColumn-java.lang.String-java.lang.班级-com.aspose.words.net.System.Data.DataTable-}
```
public DataColumn(String name, 班级 type, System.Data.DataTable table)
```


初始化一个新的实例[DataColumn](../../com.aspose.words.net.system.data/datacolumn)类使用指定的列名、数据类型和它所属的数据表。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 数据列的名称 |
| type | java.lang.班级 | 数据类型 |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable) | 此列所属的表 |

### areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet) {#areColumnSetsTheSame-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---}
```
public static boolean areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| columnSet | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) |  |
| compareSet | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) |  |

**退货:**
布尔值
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
### getAllowDBNull() {#getAllowDBNull--}
```
public boolean getAllowDBNull()
```


获取一个值，该值指示此列中是否允许属于该表的行的空值。

**退货:**
boolean - 如果允许 null 值，则为 true；否则为假。默认值为真。
### getAutoIncrement() {#getAutoIncrement--}
```
public boolean getAutoIncrement()
```


获取一个值，该值指示该列是否为添加到表中的新行自动增加该列的值。

**退货:**
boolean - 如果列的值自动增加，则为 true；否则为假。默认值为假。
### getAutoIncrementSeed() {#getAutoIncrementSeed--}
```
public long getAutoIncrementSeed()
```


获取具有它的列的起始值[getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn\#getAutoIncrement--) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn\#setAutoIncrement-boolean-)属性设置为真。

**退货:**
 long - 的起始值[getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn\#getAutoIncrement--) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn\#setAutoIncrement-boolean-)特征。
### getAutoIncrementStep() {#getAutoIncrementStep--}
```
public long getAutoIncrementStep()
```


获取列使用的增量及其[getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn\#getAutoIncrement--) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn\#setAutoIncrement-boolean-)属性设置为真。

**退货:**
long - 列值自动递增的数字。默认值为 1。
### getCaption() {#getCaption--}
```
public String getCaption()
```


获取列的标题。

**退货:**
 java.lang.String - 列的标题。如果未设置，则返回[getColumnName()](../../com.aspose.words.net.system.data/datacolumn\#getColumnName--) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn\#setColumnName-java.lang.String-)价值。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getColumnMapping() {#getColumnMapping--}
```
public int getColumnMapping()
```


获取[Mapping类型](../../com.aspose.words.net.system.data/mappingtype)的列。

**退货:**
int - 其中之一[Mapping类型](../../com.aspose.words.net.system.data/mappingtype)价值观。返回值是以下之一[Mapping类型](../../com.aspose.words.net.system.data/mappingtype)常数。
### getColumnName() {#getColumnName--}
```
public String getColumnName()
```


获取列中的名称[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection).

**退货:**
java.lang.String - 列的名称。
### getData类型() {#getData类型--}
```
public 班级 getData类型()
```


获取存储在列中的数据类型。

**退货:**
java.lang.班级 - 表示列数据类型的 java.lang.班级 对象。
### getDefaultValue() {#getDefaultValue--}
```
public Object getDefaultValue()
```


创建新行时获取列的默认值。

**退货:**
 java.lang.Object - 适合列的值[getData类型()](../../com.aspose.words.net.system.data/datacolumn\#getData类型--) / [setData类型(java.lang.班级)](../../com.aspose.words.net.system.data/datacolumn\#setData类型-java.lang.班级-).
### getExpression() {#getExpression--}
```
public String getExpression()
```


获取用于筛选行、计算列中的值或创建聚合列的表达式。

**退货:**
java.lang.String - 计算列值或创建聚合列的表达式。表达式的返回类型由[getData类型()](../../com.aspose.words.net.system.data/datacolumn\#getData类型--) / [setData类型(java.lang.班级)](../../com.aspose.words.net.system.data/datacolumn\#setData类型-java.lang.班级-)的列。
### getMaxLength() {#getMaxLength--}
```
public int getMaxLength()
```


获取文本列的最大长度。

**退货:**
int - 列的最大长度（以字符为单位）。如果列没有最大长度，则值为 -1（默认值）。
### getNamespace() {#getNamespace--}
```
public String getNamespace()
```


获取命名空间[DataColumn](../../com.aspose.words.net.system.data/datacolumn).

**退货:**
 java.lang.String - 的命名空间[DataColumn](../../com.aspose.words.net.system.data/datacolumn).
### getOrdinal() {#getOrdinal--}
```
public int getOrdinal()
```


获取列在[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection)收藏。

**退货:**
int - 列的位置。如果列不是集合的成员，则获取 -1。
### getPrefix() {#getPrefix--}
```
public String getPrefix()
```


获取一个 XML 前缀，该前缀为[DataTable](../../com.aspose.words.net.system.data/datatable).

**退货:**
 java.lang.String - 的 XML 前缀[DataTable](../../com.aspose.words.net.system.data/datatable)命名空间。
### getReadOnly() {#getReadOnly--}
```
public boolean getReadOnly()
```


获取一个值，该值指示列是否允许在将行添加到表后立即进行更改。

**退货:**
boolean - 如果该列是只读的，则为 true；否则为假。默认值为假。
### getTable() {#getTable--}
```
public System.Data.DataTable getTable()
```


获取[DataTable](../../com.aspose.words.net.system.data/datatable)该列所属的列。

**退货:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - 这[DataTable](../../com.aspose.words.net.system.data/datatable)那个[DataColumn](../../com.aspose.words.net.system.data/datacolumn)属于。
### getUnique() {#getUnique--}
```
public boolean getUnique()
```


获取一个值，该值指示列的每一行中的值是否必须唯一。

**退货:**
boolean - 如果值必须是唯一的，则为 true；否则为假。默认值为假。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isReadOnly() {#isReadOnly--}
```
public boolean isReadOnly()
```




**退货:**
布尔值
### isUnique() {#isUnique--}
```
public boolean isUnique()
```




**退货:**
布尔值
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setAllowDBNull(boolean value) {#setAllowDBNull-boolean-}
```
public void setAllowDBNull(boolean value)
```


设置一个值，该值指示此列中是否允许属于该表的行的空值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 如果允许 null 值，则为 true；否则为假。默认值为真。 |

### setAutoIncrement(boolean value) {#setAutoIncrement-boolean-}
```
public void setAutoIncrement(boolean value)
```


设置一个值，该值指示列是否为添加到表中的新行自动增加列的值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 如果列的值自动增加，则为 true；否则为假。默认值为假。 |

### setAutoIncrementSeed(long value) {#setAutoIncrementSeed-long-}
```
public void setAutoIncrementSeed(long value)
```


设置具有它的列的起始值[getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn\#getAutoIncrement--) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn\#setAutoIncrement-boolean-)属性设置为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | long | 的起始值[getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn\#getAutoIncrement--) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn\#setAutoIncrement-boolean-)特征。 |

### setAutoIncrementStep(long value) {#setAutoIncrementStep-long-}
```
public void setAutoIncrementStep(long value)
```


设置列使用的增量及其[getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn\#getAutoIncrement--) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn\#setAutoIncrement-boolean-)属性设置为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | long | 列值自动递增的数字。默认值为 1。 |

### setCaption(String value) {#setCaption-java.lang.String-}
```
public void setCaption(String value)
```


设置列的标题。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 列的标题。如果未设置，则返回[getColumnName()](../../com.aspose.words.net.system.data/datacolumn\#getColumnName--) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn\#setColumnName-java.lang.String-)价值。 |

### setColumnMapping(int value) {#setColumnMapping-int-}
```
public void setColumnMapping(int value)
```


设置[Mapping类型](../../com.aspose.words.net.system.data/mappingtype)的列。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 中的一个[Mapping类型](../../com.aspose.words.net.system.data/mappingtype)价值观。该值必须是以下之一[Mapping类型](../../com.aspose.words.net.system.data/mappingtype)常数。 |

### setColumnName(String value) {#setColumnName-java.lang.String-}
```
public void setColumnName(String value)
```


设置列的名称[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 列的名称。 |

### setData类型(班级 value) {#setData类型-java.lang.班级-}
```
public void setData类型(班级 value)
```


设置存储在列中的数据类型。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.班级 | 表示列数据类型的 java.lang.班级 对象。 |

### setDefaultValue(Object value) {#setDefaultValue-java.lang.Object-}
```
public void setDefaultValue(Object value)
```


创建新行时设置列的默认值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.Object | 适合列的值[getData类型()](../../com.aspose.words.net.system.data/datacolumn\#getData类型--) / [setData类型(java.lang.班级)](../../com.aspose.words.net.system.data/datacolumn\#setData类型-java.lang.班级-). |

### setMaxLength(int value) {#setMaxLength-int-}
```
public void setMaxLength(int value)
```


设置文本列的最大长度。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 列的最大长度（以字符为单位）。如果列没有最大长度，则值为 -1（默认值）。 |

### setNamespace(String value) {#setNamespace-java.lang.String-}
```
public void setNamespace(String value)
```


设置命名空间[DataColumn](../../com.aspose.words.net.system.data/datacolumn).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 的命名空间[DataColumn](../../com.aspose.words.net.system.data/datacolumn). |

### setOrdinal(int ordinal) {#setOrdinal-int-}
```
public void setOrdinal(int ordinal)
```


改变序数或位置[DataColumn](../../com.aspose.words.net.system.data/datacolumn)到指定的序数或位置。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ordinal | int | 指定的序数。 |

### setPrefix(String value) {#setPrefix-java.lang.String-}
```
public void setPrefix(String value)
```


设置一个 XML 前缀，为[DataTable](../../com.aspose.words.net.system.data/datatable).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 的 XML 前缀[DataTable](../../com.aspose.words.net.system.data/datatable)命名空间。 |

### setReadOnly(boolean value) {#setReadOnly-boolean-}
```
public void setReadOnly(boolean value)
```


设置一个值，该值指示列是否允许在将行添加到表后立即进行更改。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 如果该列是只读的，则为 true；否则为假。默认值为假。 |

### setUnique(boolean value) {#setUnique-boolean-}
```
public void setUnique(boolean value)
```


设置一个值，该值指示列的每一行中的值是否必须唯一。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 如果值必须是唯一的，则为 true；否则为假。默认值为假。 |

### toString() {#toString--}
```
public String toString()
```


获取[getExpression()](../../com.aspose.words.net.system.data/datacolumn\#getExpression--)列的，如果存在的话。

**退货:**
 java.lang.String - 的[getExpression()](../../com.aspose.words.net.system.data/datacolumn\#getExpression--)值，如果设置了属性；否则，[getColumnName()](../../com.aspose.words.net.system.data/datacolumn\#getColumnName--) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn\#setColumnName-java.lang.String-)财产。
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
