---
title: "DataRelation"
linktitle: "DataRelation"
second_title: "Aspose.Words für Java"
description: "Stellt eine Eltern/Kind-Beziehung zwischen zwei DataTable-Objekten in Java dar."
type: docs
weight: 18
url: /de/java/com.aspose.words.net.system.data/datarelation/
---

**Inheritance:**
java.lang.Object
```
public class DataRelation
```

Stellt eine Eltern/Kind-Beziehung zwischen zwei [DataTable](../../com.aspose.words.net.system.data/datatable/) Objekten dar.
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String) | Initialisiert eine neue Instanz der Klasse [DataRelation](../../com.aspose.words.net.system.data/datarelation/) mit dem angegebenen Namen, den Eltern- und Kind-Tabellen sowie passenden Arrays von Eltern- und Kind-Spalten. |
| [DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---boolean) | Initialisiert eine neue Instanz der Klasse [DataRelation](../../com.aspose.words.net.system.data/datarelation/) mit dem angegebenen Namen, passenden Arrays von Eltern- und Kind-[DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten und einem Wert, der angibt, ob Einschränkungen erstellt werden sollen. |
| [DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean) | Initialisiert eine neue Instanz der Klasse [DataRelation](../../com.aspose.words.net.system.data/datarelation/) mit dem angegebenen Namen, den Eltern- und Kind-[DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten und einem Wert, der angibt, ob Einschränkungen erstellt werden sollen. |
| [DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Initialisiert eine neue Instanz der Klasse [DataRelation](../../com.aspose.words.net.system.data/datarelation/) mit dem angegebenen [DataRelation](../../com.aspose.words.net.system.data/datarelation/)-Namen sowie den Eltern- und Kind-[DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) |  |
| [getChildColumnNames()](#getChildColumnNames) |  |
| [getChildColumns()](#getChildColumns) | Ruft die Kind-[DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekte dieser Relation ab. |
| [getChildKey()](#getChildKey) |  |
| [getChildKeyConstraint()](#getChildKeyConstraint) | Ruft die [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) für die Relation ab. |
| [getChildTable()](#getChildTable) | Ruft die Kindtabelle dieser Relation ab. |
| [getChildTableName()](#getChildTableName) |  |
| [getDataSet()](#getDataSet) | Ruft das [DataSet](../../com.aspose.words.net.system.data/dataset/) ab, zu dem die [DataRelation](../../com.aspose.words.net.system.data/datarelation/) gehört. |
| [getParentColumnNames()](#getParentColumnNames) |  |
| [getParentColumns()](#getParentColumns) | Ruft ein Array von [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten ab, die die Elternspalten dieser [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sind. |
| [getParentKey()](#getParentKey) |  |
| [getParentKeyConstraint()](#getParentKeyConstraint) | Ruft die [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) ab, die garantiert, dass Werte in der Elternspalte einer [DataRelation](../../com.aspose.words.net.system.data/datarelation/) eindeutig sind. |
| [getParentTable()](#getParentTable) | Ruft die Eltern-[DataTable](../../com.aspose.words.net.system.data/datatable/) dieser [DataRelation](../../com.aspose.words.net.system.data/datarelation/) ab. |
| [getParentTableName()](#getParentTableName) |  |
| [getRelationName()](#getRelationName) | Ruft den Namen ab, der verwendet wird, um eine [DataRelation](../../com.aspose.words.net.system.data/datarelation/) aus der [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) zu erhalten. |
| [hashCode()](#hashCode) |  |
| [setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint)](#setChildKeyConstraint-com.aspose.words.net.System.Data.ForeignKeyConstraint) |  |
| [setNested(boolean value)](#setNested-boolean) | Legt einen Wert fest, der angibt, ob [DataRelation](../../com.aspose.words.net.system.data/datarelation/) Objekte verschachtelt sind. |
| [setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint)](#setParentKeyConstraint-com.aspose.words.net.System.Data.UniqueConstraint) |  |
### DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String}
```
public DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)
```


Initialisiert eine neue Instanz der Klasse [DataRelation](../../com.aspose.words.net.system.data/datarelation/) mit dem angegebenen Namen, den Eltern- und Kind-Tabellen sowie passenden Arrays von Eltern- und Kind-Spalten.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relationName | java.lang.String | Der Name der DataRelation. Wenn null oder ein leerer String (""), wird ein Standardname vergeben, wenn das erstellte Objekt zur DataRelationCollection hinzugefügt wird. |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Die übergeordnete Tabelle in der Beziehung. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Die untergeordnete Tabelle in der Beziehung. |
| parentColumnNames | java.lang.String[] | Der Name der übergeordneten DataColumn in der Beziehung. |
| childColumnNames | java.lang.String[] | Die untergeordneten DataColumn(s) in der Beziehung. |

### DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---boolean}
```
public DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints)
```


Initialisiert eine neue Instanz der Klasse [DataRelation](../../com.aspose.words.net.system.data/datarelation/) mit dem angegebenen Namen, passenden Arrays von Eltern- und Kind-[DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten und einem Wert, der angibt, ob Einschränkungen erstellt werden sollen.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relationName | java.lang.String | Der Name der Relation. Wenn null oder ein leerer String (""), wird ein Standardname vergeben, wenn das erstellte Objekt zur [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) hinzugefügt wird. |
| parentColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Ein Array von übergeordneten [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) Objekten. |
| childColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Ein Array von untergeordneten [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) Objekten. |
| createConstraints | boolean | Ein Wert, der angibt, ob Einschränkungen erstellt werden sollen. true, wenn Einschränkungen erstellt werden. Andernfalls false. |

### DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean}
```
public DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)
```


Initialisiert eine neue Instanz der Klasse [DataRelation](../../com.aspose.words.net.system.data/datarelation/) mit dem angegebenen Namen, den Eltern- und Kind-[DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten und einem Wert, der angibt, ob Einschränkungen erstellt werden sollen.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relationName | java.lang.String | Der Name der Relation. Wenn null oder ein leerer String (""), wird ein Standardname vergeben, wenn das erstellte Objekt zur [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) hinzugefügt wird. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Die übergeordnete [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in der Relation. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Die untergeordnete [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in der Relation. |
| createConstraints | boolean | Ein Wert, der angibt, ob Einschränkungen erstellt werden. true, wenn Einschränkungen erstellt werden. Andernfalls false. |

### DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Initialisiert eine neue Instanz der Klasse [DataRelation](../../com.aspose.words.net.system.data/datarelation/) mit dem angegebenen [DataRelation](../../com.aspose.words.net.system.data/datarelation/)-Namen sowie den Eltern- und Kind-[DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relationName | java.lang.String | Der Name der [DataRelation](../../com.aspose.words.net.system.data/datarelation/). Wenn null oder ein leerer String (""), wird ein Standardname vergeben, wenn das erstellte Objekt zur [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) hinzugefügt wird. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Die übergeordnete [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in der Beziehung. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Die untergeordnete [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in der Beziehung. |

### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getChildColumnNames() {#getChildColumnNames}
```
public String[] getChildColumnNames()
```




**Returns:**
java.lang.String[] - die Namen der untergeordneten DataColumn dieser Relation.
### getChildColumns() {#getChildColumns}
```
public System.Data.DataColumn[] getChildColumns()
```


Ruft die Kind-[DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekte dieser Relation ab.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Ein Array von [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten.
### getChildKey() {#getChildKey}
```
public System.Data.DataKey getChildKey()
```




**Returns:**
[DataKey](../../com.aspose.words.net.system.data/datakey/)
### getChildKeyConstraint() {#getChildKeyConstraint}
```
public System.Data.ForeignKeyConstraint getChildKeyConstraint()
```


Ruft die [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) für die Relation ab.

**Returns:**
[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) - A [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/).
### getChildTable() {#getChildTable}
```
public System.Data.DataTable getChildTable()
```


Ruft die Kindtabelle dieser Relation ab.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the child table of the relation.
### getChildTableName() {#getChildTableName}
```
public String getChildTableName()
```




**Returns:**
java.lang.String - der Name der untergeordneten DataTable dieser DataRelation.
### getDataSet() {#getDataSet}
```
public System.Data.DataSet getDataSet()
```


Ruft das [DataSet](../../com.aspose.words.net.system.data/dataset/) ab, zu dem die [DataRelation](../../com.aspose.words.net.system.data/datarelation/) gehört.

**Returns:**
[DataSet](../../com.aspose.words.net.system.data/dataset/) - A [DataSet](../../com.aspose.words.net.system.data/dataset/) to which the [DataRelation](../../com.aspose.words.net.system.data/datarelation/) belongs.
### getParentColumnNames() {#getParentColumnNames}
```
public String[] getParentColumnNames()
```




**Returns:**
java.lang.String[] - die Namen der übergeordneten DataColumn dieser Relation.
### getParentColumns() {#getParentColumns}
```
public System.Data.DataColumn[] getParentColumns()
```


Ruft ein Array von [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten ab, die die Elternspalten dieser [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sind.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Ein Array von [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) Objekten, die die übergeordneten Spalten dieser [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sind.
### getParentKey() {#getParentKey}
```
public System.Data.DataKey getParentKey()
```




**Returns:**
[DataKey](../../com.aspose.words.net.system.data/datakey/)
### getParentKeyConstraint() {#getParentKeyConstraint}
```
public System.Data.UniqueConstraint getParentKeyConstraint()
```


Ruft die [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) ab, die garantiert, dass Werte in der Elternspalte einer [DataRelation](../../com.aspose.words.net.system.data/datarelation/) eindeutig sind.

**Returns:**
[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) - A [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) that makes sure that values in a parent column are unique.
### getParentTable() {#getParentTable}
```
public System.Data.DataTable getParentTable()
```


Ruft die Eltern-[DataTable](../../com.aspose.words.net.system.data/datatable/) dieser [DataRelation](../../com.aspose.words.net.system.data/datarelation/) ab.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the parent table of this relation.
### getParentTableName() {#getParentTableName}
```
public String getParentTableName()
```




**Returns:**
java.lang.String - der Name der übergeordneten DataTable dieser DataRelation.
### getRelationName() {#getRelationName}
```
public String getRelationName()
```


Ruft den Namen ab, der verwendet wird, um eine [DataRelation](../../com.aspose.words.net.system.data/datarelation/) aus der [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) zu erhalten.

**Returns:**
java.lang.String - Der Name einer [DataRelation](../../com.aspose.words.net.system.data/datarelation/).
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint) {#setChildKeyConstraint-com.aspose.words.net.System.Data.ForeignKeyConstraint}
```
public void setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| childKeyConstraint | [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) |  |

### setNested(boolean value) {#setNested-boolean}
```
public void setNested(boolean value)
```


Legt einen Wert fest, der angibt, ob [DataRelation](../../com.aspose.words.net.system.data/datarelation/) Objekte verschachtelt sind.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | boolean | true, wenn [DataRelation](../../com.aspose.words.net.system.data/datarelation/) Objekte verschachtelt sind; andernfalls false. |

### setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint) {#setParentKeyConstraint-com.aspose.words.net.System.Data.UniqueConstraint}
```
public void setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| parentKeyConstraint | [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) |  |

