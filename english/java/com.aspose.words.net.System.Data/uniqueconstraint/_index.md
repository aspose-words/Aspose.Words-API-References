---
title: UniqueConstraint
second_title: Aspose.Words for Java API Reference
description: Represents a restriction on a set of columns in which all values must be unique.
type: docs
weight: 32
url: /java/com.aspose.words.net.system.data/uniqueconstraint/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Constraint](../../com.aspose.words.net.system.data/constraint)
```
public class UniqueConstraint extends System.Data.Constraint
```

Represents a restriction on a set of columns in which all values must be unique.
## Constructors

| Constructor | Description |
| --- | --- |
| [UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey)](#UniqueConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---boolean-) | Initializes a new instance of the [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) class with the specified name, an array of [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects to constrain, and a value specifying whether the constraint is a primary key. |
| [UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---boolean-) | Initializes a new instance of the [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) class with an array of [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects to constrain, and a value specifying whether the constraint is a primary key. |
| [UniqueConstraint(System.Data.DataColumn[] columns)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---) | Initializes a new instance of the [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) class with the given array of [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects. |
| [UniqueConstraint(System.Data.DataColumn column)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn-) | Initializes a new instance of the [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) class with the specified [DataColumn](../../com.aspose.words.net.system.data/datacolumn). |
## Methods

| Method | Description |
| --- | --- |
| [hashCode()](#hashCode--) |  |
| [equals(Object key2)](#equals-java.lang.Object-) | Compares this constraint to a second to determine if both are identical. |
| [getColumns()](#getColumns--) | Gets the array of columns that this constraint affects. |
| [isPrimaryKey()](#isPrimaryKey--) | Gets a value indicating whether or not the constraint is on a primary key. |
| [getTable()](#getTable--) | Gets the table to which this constraint belongs. |
### UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey) {#UniqueConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---boolean-}
```
public UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey)
```


Initializes a new instance of the [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) class with the specified name, an array of [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects to constrain, and a value specifying whether the constraint is a primary key.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the constraint. |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) | An array of [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects to constrain. |
| isPrimaryKey | boolean | true to indicate that the constraint is a primary key; otherwise, false. |

### UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---boolean-}
```
public UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey)
```


Initializes a new instance of the [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) class with an array of [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects to constrain, and a value specifying whether the constraint is a primary key.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) | An array of [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects to constrain. |
| isPrimaryKey | boolean | true to indicate that the constraint is a primary key; otherwise, false. |

### UniqueConstraint(System.Data.DataColumn[] columns) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---}
```
public UniqueConstraint(System.Data.DataColumn[] columns)
```


Initializes a new instance of the [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) class with the given array of [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) | The array of [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects to constrain. |

### UniqueConstraint(System.Data.DataColumn column) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn-}
```
public UniqueConstraint(System.Data.DataColumn column)
```


Initializes a new instance of the [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) class with the specified [DataColumn](../../com.aspose.words.net.system.data/datacolumn).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | The [DataColumn](../../com.aspose.words.net.system.data/datacolumn) to constrain. |

### hashCode() {#hashCode--}
```
public int hashCode()
```




**Returns:**
int
### equals(Object key2) {#equals-java.lang.Object-}
```
public boolean equals(Object key2)
```


Compares this constraint to a second to determine if both are identical.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key2 | java.lang.Object | The object to which this [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) is compared. |

**Returns:**
boolean - true, if the contraints are equal; otherwise, false.
### getColumns() {#getColumns--}
```
public System.Data.DataColumn[] getColumns()
```


Gets the array of columns that this constraint affects.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - An array of [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects.
### isPrimaryKey() {#isPrimaryKey--}
```
public boolean isPrimaryKey()
```


Gets a value indicating whether or not the constraint is on a primary key.

**Returns:**
boolean - true, if the constraint is on a primary key; otherwise, false.
### getTable() {#getTable--}
```
public System.Data.DataTable getTable()
```


Gets the table to which this constraint belongs.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - The [DataTable](../../com.aspose.words.net.system.data/datatable) to which the constraint belongs.
