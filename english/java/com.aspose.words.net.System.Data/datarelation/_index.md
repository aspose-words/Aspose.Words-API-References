---
title: DataRelation
second_title: Aspose.Words for Java API Reference
description: Represents a parent/child relationship between two  objects.
type: docs
weight: 18
url: /java/com.aspose.words.net.system.data/datarelation/
---

**Inheritance:**
java.lang.Object
```
public class DataRelation
```

Represents a parent/child relationship between two [DataTable](../../com.aspose.words.net.system.data/datatable) objects.
## Constructors

| Constructor | Description |
| --- | --- |
| [DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String---) | Initializes a new instance of the [DataRelation](../../com.aspose.words.net.system.data/datarelation) class using the specified name, parent and child tables, matched arrays of parent and child columns. |
| [DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---boolean-) | Initializes a new instance of the [DataRelation](../../com.aspose.words.net.system.data/datarelation) class using the specified name, matched arrays of parent and child [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects, and value that indicates whether to create constraints. |
| [DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean-) | Initializes a new instance of the [DataRelation](../../com.aspose.words.net.system.data/datarelation) class using the specified name, parent and child [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects, and a value that indicates whether to create constraints. |
| [DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-) | Initializes a new instance of the [DataRelation](../../com.aspose.words.net.system.data/datarelation) class using the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation) name, and parent and child [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects. |
## Methods

| Method | Description |
| --- | --- |
| [getRelationName()](#getRelationName--) | Gets the name used to retrieve a [DataRelation](../../com.aspose.words.net.system.data/datarelation) from the [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection). |
| [getParentTableName()](#getParentTableName--) |  |
| [getChildTableName()](#getChildTableName--) |  |
| [getParentTable()](#getParentTable--) | Gets the parent [DataTable](../../com.aspose.words.net.system.data/datatable) of this [DataRelation](../../com.aspose.words.net.system.data/datarelation). |
| [getChildTable()](#getChildTable--) | Gets the child table of this relation. |
| [getParentColumnNames()](#getParentColumnNames--) |  |
| [getChildColumnNames()](#getChildColumnNames--) |  |
| [getParentColumns()](#getParentColumns--) | Gets an array of [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects that are the parent columns of this [DataRelation](../../com.aspose.words.net.system.data/datarelation). |
| [getChildColumns()](#getChildColumns--) | Gets the child [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects of this relation. |
| [setNested(boolean value)](#setNested-boolean-) | Sets a value that indicates whether [DataRelation](../../com.aspose.words.net.system.data/datarelation) objects are nested. |
| [getParentKeyConstraint()](#getParentKeyConstraint--) | Gets the [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) that guarantees that values in the parent column of a [DataRelation](../../com.aspose.words.net.system.data/datarelation) are unique. |
| [setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint)](#setParentKeyConstraint-com.aspose.words.net.System.Data.UniqueConstraint-) |  |
| [getChildKeyConstraint()](#getChildKeyConstraint--) | Gets the [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) for the relation. |
| [setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint)](#setChildKeyConstraint-com.aspose.words.net.System.Data.ForeignKeyConstraint-) |  |
| [getChildKey()](#getChildKey--) |  |
| [getParentKey()](#getParentKey--) |  |
| [getDataSet()](#getDataSet--) | Gets the [DataSet](../../com.aspose.words.net.system.data/dataset) to which the [DataRelation](../../com.aspose.words.net.system.data/datarelation) belongs. |
| [hashCode()](#hashCode--) |  |
| [equals(Object obj)](#equals-java.lang.Object-) |  |
### DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String---}
```
public DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)
```


Initializes a new instance of the [DataRelation](../../com.aspose.words.net.system.data/datarelation) class using the specified name, parent and child tables, matched arrays of parent and child columns.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| relationName | java.lang.String | The name of the DataRelation. If null or an empty string (""), a default name will be given when the created object is added to the DataRelationCollection. |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable) | The parent table in the relationship. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable) | The child table in the relationship. |
| parentColumnNames | java.lang.String[] | The parent DataColumn's name in the relationship. |
| childColumnNames | java.lang.String[] | The child DataColumn;s in the relationship. |

### DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---boolean-}
```
public DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints)
```


Initializes a new instance of the [DataRelation](../../com.aspose.words.net.system.data/datarelation) class using the specified name, matched arrays of parent and child [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects, and value that indicates whether to create constraints.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| relationName | java.lang.String | The name of the relation. If null or an empty string (""), a default name will be given when the created object is added to the [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection). |
| parentColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) | An array of parent [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects. |
| childColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) | An array of child [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects. |
| createConstraints | boolean | A value that indicates whether to create constraints. true, if constraints are created. Otherwise, false. |

### DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean-}
```
public DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)
```


Initializes a new instance of the [DataRelation](../../com.aspose.words.net.system.data/datarelation) class using the specified name, parent and child [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects, and a value that indicates whether to create constraints.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| relationName | java.lang.String | The name of the relation. If null or an empty string (""), a default name will be given when the created object is added to the [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection). |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | The parent [DataColumn](../../com.aspose.words.net.system.data/datacolumn) in the relation. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | The child [DataColumn](../../com.aspose.words.net.system.data/datacolumn) in the relation. |
| createConstraints | boolean | A value that indicates whether constraints are created. true, if constraints are created. Otherwise, false. |

### DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-}
```
public DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Initializes a new instance of the [DataRelation](../../com.aspose.words.net.system.data/datarelation) class using the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation) name, and parent and child [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| relationName | java.lang.String | The name of the [DataRelation](../../com.aspose.words.net.system.data/datarelation). If null or an empty string (""), a default name will be given when the created object is added to the [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection). |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | The parent [DataColumn](../../com.aspose.words.net.system.data/datacolumn) in the relationship. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | The child [DataColumn](../../com.aspose.words.net.system.data/datacolumn) in the relationship. |

### getRelationName() {#getRelationName--}
```
public String getRelationName()
```


Gets the name used to retrieve a [DataRelation](../../com.aspose.words.net.system.data/datarelation) from the [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection).

**Returns:**
java.lang.String - The name of the a [DataRelation](../../com.aspose.words.net.system.data/datarelation).
### getParentTableName() {#getParentTableName--}
```
public String getParentTableName()
```




**Returns:**
java.lang.String - the parent DataTable's name of this DataRelation.
### getChildTableName() {#getChildTableName--}
```
public String getChildTableName()
```




**Returns:**
java.lang.String - the child DataTable's name of this DataRelation.
### getParentTable() {#getParentTable--}
```
public System.Data.DataTable getParentTable()
```


Gets the parent [DataTable](../../com.aspose.words.net.system.data/datatable) of this [DataRelation](../../com.aspose.words.net.system.data/datarelation).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - A [DataTable](../../com.aspose.words.net.system.data/datatable) that is the parent table of this relation.
### getChildTable() {#getChildTable--}
```
public System.Data.DataTable getChildTable()
```


Gets the child table of this relation.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - A [DataTable](../../com.aspose.words.net.system.data/datatable) that is the child table of the relation.
### getParentColumnNames() {#getParentColumnNames--}
```
public String[] getParentColumnNames()
```




**Returns:**
java.lang.String[] - the parent DataColumn names of this relation.
### getChildColumnNames() {#getChildColumnNames--}
```
public String[] getChildColumnNames()
```




**Returns:**
java.lang.String[] - the child DataColumn names of this relation.
### getParentColumns() {#getParentColumns--}
```
public System.Data.DataColumn[] getParentColumns()
```


Gets an array of [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects that are the parent columns of this [DataRelation](../../com.aspose.words.net.system.data/datarelation).

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - An array of [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects that are the parent columns of this [DataRelation](../../com.aspose.words.net.system.data/datarelation).
### getChildColumns() {#getChildColumns--}
```
public System.Data.DataColumn[] getChildColumns()
```


Gets the child [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects of this relation.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - An array of [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects.
### setNested(boolean value) {#setNested-boolean-}
```
public void setNested(boolean value)
```


Sets a value that indicates whether [DataRelation](../../com.aspose.words.net.system.data/datarelation) objects are nested.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | true, if [DataRelation](../../com.aspose.words.net.system.data/datarelation) objects are nested; otherwise, false. |

### getParentKeyConstraint() {#getParentKeyConstraint--}
```
public System.Data.UniqueConstraint getParentKeyConstraint()
```


Gets the [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) that guarantees that values in the parent column of a [DataRelation](../../com.aspose.words.net.system.data/datarelation) are unique.

**Returns:**
[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) - A [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) that makes sure that values in a parent column are unique.
### setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint) {#setParentKeyConstraint-com.aspose.words.net.System.Data.UniqueConstraint-}
```
public void setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| parentKeyConstraint | [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) |  |

### getChildKeyConstraint() {#getChildKeyConstraint--}
```
public System.Data.ForeignKeyConstraint getChildKeyConstraint()
```


Gets the [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) for the relation.

**Returns:**
[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) - A [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint).
### setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint) {#setChildKeyConstraint-com.aspose.words.net.System.Data.ForeignKeyConstraint-}
```
public void setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| childKeyConstraint | [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) |  |

### getChildKey() {#getChildKey--}
```
public System.Data.DataKey getChildKey()
```




**Returns:**
[DataKey](../../com.aspose.words.net.system.data/datakey)
### getParentKey() {#getParentKey--}
```
public System.Data.DataKey getParentKey()
```




**Returns:**
[DataKey](../../com.aspose.words.net.system.data/datakey)
### getDataSet() {#getDataSet--}
```
public System.Data.DataSet getDataSet()
```


Gets the [DataSet](../../com.aspose.words.net.system.data/dataset) to which the [DataRelation](../../com.aspose.words.net.system.data/datarelation) belongs.

**Returns:**
[DataSet](../../com.aspose.words.net.system.data/dataset) - A [DataSet](../../com.aspose.words.net.system.data/dataset) to which the [DataRelation](../../com.aspose.words.net.system.data/datarelation) belongs.
### hashCode() {#hashCode--}
```
public int hashCode()
```




**Returns:**
int
### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
