---
title: "UniqueConstraint"
linktitle: "UniqueConstraint"
second_title: "Aspose.Words für Java"
description: "Stellt eine Einschränkung für ein Set von Spalten dar, bei der alle Werte in Java eindeutig sein müssen."
type: docs
weight: 32
url: /de/java/com.aspose.words.net.system.data/uniqueconstraint/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Constraint](../../com.aspose.words.net.system.data/constraint/)
```
public class UniqueConstraint extends System.Data.Constraint
```

Stellt eine Einschränkung für eine Menge von Spalten dar, bei denen alle Werte eindeutig sein müssen.
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey)](#UniqueConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---boolean) | Initialisiert eine neue Instanz der Klasse [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) mit dem angegebenen Namen, einem Array von [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten, die eingeschränkt werden sollen, und einem Wert, der angibt, ob die Einschränkung ein Primärschlüssel ist. |
| [UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---boolean) | Initialisiert eine neue Instanz der Klasse [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) mit einem Array von [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten, die eingeschränkt werden sollen, und einem Wert, der angibt, ob die Einschränkung ein Primärschlüssel ist. |
| [UniqueConstraint(System.Data.DataColumn[] columns)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn) | Initialisiert eine neue Instanz der Klasse [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) mit dem angegebenen Array von [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten. |
| [UniqueConstraint(System.Data.DataColumn column)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn) | Initialisiert eine neue Instanz der Klasse [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) mit der angegebenen [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [equals(Object key2)](#equals-java.lang.Object) | Vergleicht diese Einschränkung mit einer zweiten, um festzustellen, ob beide identisch sind. |
| [getColumns()](#getColumns) | Gibt das Array von Spalten zurück, die von dieser Einschränkung betroffen sind. |
| [getConstraintName()](#getConstraintName) | Der Name einer Einschränkung in der [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
| [getTable()](#getTable) | Gibt die Tabelle zurück, zu der diese Einschränkung gehört. |
| [hashCode()](#hashCode) |  |
| [isPrimaryKey()](#isPrimaryKey) | Gibt einen Wert zurück, der angibt, ob die Einschränkung ein Primärschlüssel ist oder nicht. |
| [setConstraintName(String value)](#setConstraintName-java.lang.String) | Der Name einer Einschränkung in der [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
### UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey) {#UniqueConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---boolean}
```
public UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey)
```


Initialisiert eine neue Instanz der Klasse [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) mit dem angegebenen Namen, einem Array von [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten, die eingeschränkt werden sollen, und einem Wert, der angibt, ob die Einschränkung ein Primärschlüssel ist.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name der Einschränkung. |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Ein Array von [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten, die eingeschränkt werden sollen. |
| isPrimaryKey | boolean | true, um anzugeben, dass die Einschränkung ein Primärschlüssel ist; andernfalls false. |

### UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---boolean}
```
public UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey)
```


Initialisiert eine neue Instanz der Klasse [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) mit einem Array von [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten, die eingeschränkt werden sollen, und einem Wert, der angibt, ob die Einschränkung ein Primärschlüssel ist.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Ein Array von [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten, die eingeschränkt werden sollen. |
| isPrimaryKey | boolean | true, um anzugeben, dass die Einschränkung ein Primärschlüssel ist; andernfalls false. |

### UniqueConstraint(System.Data.DataColumn[] columns) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn}
```
public UniqueConstraint(System.Data.DataColumn[] columns)
```


Initialisiert eine neue Instanz der Klasse [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) mit dem angegebenen Array von [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Das Array von [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) Objekten zum Einschränken. |

### UniqueConstraint(System.Data.DataColumn column) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn}
```
public UniqueConstraint(System.Data.DataColumn column)
```


Initialisiert eine neue Instanz der Klasse [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) mit der angegebenen [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Die [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) zum Einschränken. |

### equals(Object key2) {#equals-java.lang.Object}
```
public boolean equals(Object key2)
```


Vergleicht diese Einschränkung mit einer zweiten, um festzustellen, ob beide identisch sind.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key2 | java.lang.Object | Das Objekt, mit dem diese [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) verglichen wird. |

**Returns:**
boolean – true, wenn die Constraints gleich sind; andernfalls false.
### getColumns() {#getColumns}
```
public System.Data.DataColumn[] getColumns()
```


Gibt das Array von Spalten zurück, die von dieser Einschränkung betroffen sind.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Ein Array von [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten.
### getConstraintName() {#getConstraintName}
```
public String getConstraintName()
```


Der Name einer Einschränkung in der [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Returns:**
java.lang.String – Der Name der [Constraint](../../com.aspose.words.net.system.data/constraint/).
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Gibt die Tabelle zurück, zu der diese Einschränkung gehört.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) to which the constraint belongs.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### isPrimaryKey() {#isPrimaryKey}
```
public boolean isPrimaryKey()
```


Gibt einen Wert zurück, der angibt, ob die Einschränkung ein Primärschlüssel ist oder nicht.

**Returns:**
boolean – true, wenn die Einschränkung auf einem Primärschlüssel liegt; andernfalls false.
### setConstraintName(String value) {#setConstraintName-java.lang.String}
```
public void setConstraintName(String value)
```


Der Name einer Einschränkung in der [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | java.lang.String | Der Name der [Constraint](../../com.aspose.words.net.system.data/constraint/). |

