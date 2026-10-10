---
title: "ForeignKeyConstraint"
linktitle: "ForeignKeyConstraint"
second_title: "Aspose.Words für Java"
description: "Stellt eine Aktionsbeschränkung dar, die auf einer Menge von Spalten in einer Primärschlüssel-/Fremdschlüssel-Beziehung durchgesetzt wird, wenn ein Wert oder eine Zeile in Java gelöscht oder aktualisiert wird."
type: docs
weight: 29
url: /de/java/com.aspose.words.net.system.data/foreignkeyconstraint/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Constraint](../../com.aspose.words.net.system.data/constraint/)
```
public class ForeignKeyConstraint extends System.Data.Constraint
```

Stellt eine Aktionsbeschränkung dar, die bei einem Satz von Spalten in einer Primärschlüssel‑/Fremdschlüssel‑Beziehung durchgesetzt wird, wenn ein Wert oder eine Zeile gelöscht oder aktualisiert wird.
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns)](#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn) | Initialisiert eine neue Instanz der Klasse [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) mit dem angegebenen Namen und Arrays von übergeordneten und untergeordneten [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten. |
| [ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#ForeignKeyConstraint-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Initialisiert eine neue Instanz der Klasse [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) mit den angegebenen übergeordneten und untergeordneten [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten. |
| [ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Initialisiert eine neue Instanz der Klasse [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) mit dem angegebenen Namen, den übergeordneten und untergeordneten [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [equals(Object key)](#equals-java.lang.Object) | Gibt einen Wert zurück, der angibt, ob das aktuelle [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) mit dem angegebenen Objekt identisch ist. |
| [getColumns()](#getColumns) | Gibt die untergeordneten Spalten dieser Einschränkung zurück. |
| [getConstraintName()](#getConstraintName) | Der Name einer Einschränkung in der [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
| [getDeleteRule()](#getDeleteRule) | Gibt die Aktion zurück, die bei dieser Einschränkung ausgeführt wird, wenn eine Zeile gelöscht wird. |
| [getRelatedColumns()](#getRelatedColumns) | Die übergeordneten Spalten dieser Einschränkung. |
| [getRelatedTable()](#getRelatedTable) | Gibt die übergeordnete Tabelle dieser Einschränkung zurück. |
| [getTable()](#getTable) | Gibt die untergeordnete Tabelle dieser Einschränkung zurück. |
| [getUpdateRule()](#getUpdateRule) | Gibt die Aktion zurück, die bei dieser Einschränkung ausgeführt wird, wenn eine Zeile aktualisiert wird. |
| [hashCode()](#hashCode) |  |
| [setConstraintName(String value)](#setConstraintName-java.lang.String) | Der Name einer Einschränkung in der [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
### ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns) {#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns)
```


Initialisiert eine neue Instanz der Klasse [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) mit dem angegebenen Namen und Arrays von übergeordneten und untergeordneten [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| constraintName | java.lang.String | Der Name des [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/). Wenn null oder ein leerer String, wird beim Hinzufügen zur Einschränkungssammlung ein Standardname vergeben. |
| parentColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Ein Array von übergeordneten [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in der Einschränkung. |
| childColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Ein Array von untergeordneten [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in der Einschränkung. |

### ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#ForeignKeyConstraint-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Initialisiert eine neue Instanz der Klasse [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) mit den angegebenen übergeordneten und untergeordneten [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Die übergeordnete [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in der Einschränkung. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Die untergeordnete [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in der Einschränkung. |

### ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Initialisiert eine neue Instanz der Klasse [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) mit dem angegebenen Namen, den übergeordneten und untergeordneten [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| constraintName | java.lang.String | Der Name der Einschränkung. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Die übergeordnete [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in der Einschränkung. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Die untergeordnete [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in der Einschränkung. |

### equals(Object key) {#equals-java.lang.Object}
```
public boolean equals(Object key)
```


Gibt einen Wert zurück, der angibt, ob das aktuelle [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) mit dem angegebenen Objekt identisch ist.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | java.lang.Object | Das Objekt, mit dem dieses [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) verglichen wird. Zwei [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) sind gleich, wenn sie dieselben Spalten einschränken. |

**Returns:**
boolean – true, wenn die Objekte identisch sind; andernfalls false.
### getColumns() {#getColumns}
```
public System.Data.DataColumn[] getColumns()
```


Gibt die untergeordneten Spalten dieser Einschränkung zurück.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] – Ein Array von [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten, die die untergeordneten Spalten der Einschränkung darstellen.
### getConstraintName() {#getConstraintName}
```
public String getConstraintName()
```


Der Name einer Einschränkung in der [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Returns:**
java.lang.String – Der Name der [Constraint](../../com.aspose.words.net.system.data/constraint/).
### getDeleteRule() {#getDeleteRule}
```
public System.Data.Rule getDeleteRule()
```


Gibt die Aktion zurück, die bei dieser Einschränkung ausgeführt wird, wenn eine Zeile gelöscht wird.

**Returns:**
[Rule](../../com.aspose.words.net.system.data/rule/) - One of the [Rule](../../com.aspose.words.net.system.data/rule/) values. The default is Cascade. The returned value is one of [Rule](../../com.aspose.words.net.system.data/rule/) constants.
### getRelatedColumns() {#getRelatedColumns}
```
public System.Data.DataColumn[] getRelatedColumns()
```


Die übergeordneten Spalten dieser Einschränkung.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Ein Array von [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) Objekten, die die übergeordneten Spalten der Einschränkung sind.
### getRelatedTable() {#getRelatedTable}
```
public System.Data.DataTable getRelatedTable()
```


Gibt die übergeordnete Tabelle dieser Einschränkung zurück.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The parent [DataTable](../../com.aspose.words.net.system.data/datatable/) of this constraint.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Gibt die untergeordnete Tabelle dieser Einschränkung zurück.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the child table in the constraint.
### getUpdateRule() {#getUpdateRule}
```
public System.Data.Rule getUpdateRule()
```


Gibt die Aktion zurück, die bei dieser Einschränkung ausgeführt wird, wenn eine Zeile aktualisiert wird.

**Returns:**
[Rule](../../com.aspose.words.net.system.data/rule/) - One of the [Rule](../../com.aspose.words.net.system.data/rule/) values. The default is Cascade. The returned value is one of [Rule](../../com.aspose.words.net.system.data/rule/) constants.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### setConstraintName(String value) {#setConstraintName-java.lang.String}
```
public void setConstraintName(String value)
```


Der Name einer Einschränkung in der [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | java.lang.String | Der Name der [Constraint](../../com.aspose.words.net.system.data/constraint/). |

