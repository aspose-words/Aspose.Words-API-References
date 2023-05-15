---
title: ForeignKeyConstraint
linktitle: ForeignKeyConstraint
second_title: Aspose.Words for Java
description: Represents an action restriction enforced on a set of columns in a primary key/foreign key relationship when a value or row is either deleted or updated in Java.
type: docs
weight: 29
url: /java/com.aspose.words.net.system.data/foreignkeyconstraint/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Constraint](../../com.aspose.words.net.system.data/constraint/)
```
public class ForeignKeyConstraint extends System.Data.Constraint
```

Represents an action restriction enforced on a set of columns in a primary key/foreign key relationship when a value or row is either deleted or updated.
## Constructors

| Constructor | Description |
| --- | --- |
| [ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns)](#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn) | Initializes a new instance of the [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) class with the specified name, and arrays of parent and child [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects. |
| [ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#ForeignKeyConstraint-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Initializes a new instance of the [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) class with the specified parent and child [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects. |
| [ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Initializes a new instance of the [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) class with the specified name, parent and child [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects. |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object key)](#equals-java.lang.Object) | Gets a value indicating whether the current [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) is identical to the specified object. |
| [getClass()](#getClass) |  |
| [getColumns()](#getColumns) | Gets the child columns of this constraint. |
| [getConstraintName()](#getConstraintName) | The name of a constraint in the [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
| [getDeleteRule()](#getDeleteRule) | Gets the action that occurs across this constraint when a row is deleted. |
| [getRelatedColumns()](#getRelatedColumns) | The parent columns of this constraint. |
| [getRelatedTable()](#getRelatedTable) | Gets the parent table of this constraint. |
| [getTable()](#getTable) | Gets the child table of this constraint. |
| [getUpdateRule()](#getUpdateRule) | Gets the action that occurs across this constraint on when a row is updated. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setConstraintName(String value)](#setConstraintName-java.lang.String) | The name of a constraint in the [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns) {#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns)
```


Initializes a new instance of the [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) class with the specified name, and arrays of parent and child [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| constraintName | java.lang.String | The name of the [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/). If null or empty string, a default name will be given when added to the constraints collection. |
| parentColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | An array of parent [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in the constraint. |
| childColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | An array of child [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in the constraint. |

### ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#ForeignKeyConstraint-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Initializes a new instance of the [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) class with the specified parent and child [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | The parent [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in the constraint. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | The child [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in the constraint. |

### ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Initializes a new instance of the [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) class with the specified name, parent and child [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| constraintName | java.lang.String | The name of the constraint. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | The parent [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in the constraint. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | The child [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in the constraint. |

### equals(Object key) {#equals-java.lang.Object}
```
public boolean equals(Object key)
```


Gets a value indicating whether the current [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) is identical to the specified object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | java.lang.Object | The object to which this [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) is compared. Two [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) are equal if they constrain the same columns. |

**Returns:**
boolean - true, if the objects are identical; otherwise, false.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getColumns() {#getColumns}
```
public System.Data.DataColumn[] getColumns()
```


Gets the child columns of this constraint.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - An array of [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects that are the child columns of the constraint.
### getConstraintName() {#getConstraintName}
```
public String getConstraintName()
```


The name of a constraint in the [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Returns:**
java.lang.String - The name of the [Constraint](../../com.aspose.words.net.system.data/constraint/).
### getDeleteRule() {#getDeleteRule}
```
public System.Data.Rule getDeleteRule()
```


Gets the action that occurs across this constraint when a row is deleted.

**Returns:**
[Rule](../../com.aspose.words.net.system.data/rule/) - One of the [Rule](../../com.aspose.words.net.system.data/rule/) values. The default is Cascade. The returned value is one of [Rule](../../com.aspose.words.net.system.data/rule/) constants.
### getRelatedColumns() {#getRelatedColumns}
```
public System.Data.DataColumn[] getRelatedColumns()
```


The parent columns of this constraint.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - An array of [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects that are the parent columns of the constraint.
### getRelatedTable() {#getRelatedTable}
```
public System.Data.DataTable getRelatedTable()
```


Gets the parent table of this constraint.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The parent [DataTable](../../com.aspose.words.net.system.data/datatable/) of this constraint.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Gets the child table of this constraint.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the child table in the constraint.
### getUpdateRule() {#getUpdateRule}
```
public System.Data.Rule getUpdateRule()
```


Gets the action that occurs across this constraint on when a row is updated.

**Returns:**
[Rule](../../com.aspose.words.net.system.data/rule/) - One of the [Rule](../../com.aspose.words.net.system.data/rule/) values. The default is Cascade. The returned value is one of [Rule](../../com.aspose.words.net.system.data/rule/) constants.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setConstraintName(String value) {#setConstraintName-java.lang.String}
```
public void setConstraintName(String value)
```


The name of a constraint in the [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the [Constraint](../../com.aspose.words.net.system.data/constraint/). |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

