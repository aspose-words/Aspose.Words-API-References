---
title: "DataTable"
linktitle: "DataTable"
second_title: "Aspose.Words für Java"
description: "Stellt eine Tabelle von In-Memory-Daten in Java dar."
type: docs
weight: 25
url: /de/java/com.aspose.words.net.system.data/datatable/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.net.System.Data.DataTableEventListener](../../com.aspose.words.net.system.data/datatableeventlistener/)
```
public class DataTable implements System.Data.DataTableEventListener
```

Stellt eine Tabelle von In‑Memory‑Daten dar.
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [DataTable()](#DataTable) | Initialisiert eine neue Instanz der Klasse [DataTable](../../com.aspose.words.net.system.data/datatable/) ohne Argumente. |
| [DataTable(String tableName)](#DataTable-java.lang.String) | Initialisiert eine neue Instanz der Klasse [DataTable](../../com.aspose.words.net.system.data/datatable/) mit dem angegebenen Tabellennamen. |
| [DataTable(ResultSet resultSet)](#DataTable-java.sql.ResultSet) | Erstellt ein Objekt, indem das angegebene ResultSet umschlossen wird. |
| [DataTable(ResultSet resultSet, String tableName)](#DataTable-java.sql.ResultSet-java.lang.String) | Erstellt ein Objekt, indem das angegebene ResultSet umschlossen wird. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [acceptChanges()](#acceptChanges) | Übernimmt alle Änderungen, die an dieser Tabelle seit dem letzten Aufruf von [acceptChanges()](../../com.aspose.words.net.system.data/datatable/\#acceptChanges) vorgenommen wurden. |
| [addEventListener(System.Data.DataTableEventListener listener)](#addEventListener-com.aspose.words.net.System.Data.DataTableEventListener) |  |
| [clearEventListneers()](#clearEventListneers) |  |
| [close()](#close) |  |
| [containsColumn(String columnName)](#containsColumn-java.lang.String) | Überprüfen, ob die angegebene Spalte existiert oder nicht |
| [getChildRelations()](#getChildRelations) | Liefert die Sammlung der untergeordneten Beziehungen für diese [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getColumnName(int index)](#getColumnName-int) | Analog für .Net DataTable.Columns[i].ColumnName |
| [getColumns()](#getColumns) | Liefert die Sammlung der Spalten, die zu dieser Tabelle gehören. |
| [getColumnsCount()](#getColumnsCount) |  |
| [getConstraints()](#getConstraints) | Liefert die Sammlung der von dieser Tabelle verwalteten Einschränkungen. |
| [getDataSet()](#getDataSet) | Liefert das [DataSet](../../com.aspose.words.net.system.data/dataset/), zu dem diese Tabelle gehört. |
| [getEnforceConstraints()](#getEnforceConstraints) |  |
| [getNamespace()](#getNamespace) | Liefert den Namensraum für die XML-Darstellung der in der [DataTable](../../com.aspose.words.net.system.data/datatable/) gespeicherten Daten. |
| [getParentRelations()](#getParentRelations) | Liefert die Sammlung der übergeordneten Beziehungen für diese [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getPrimaryKey()](#getPrimaryKey) | Liefert ein Array von Spalten, die als Primärschlüssel für die Datentabelle fungieren. |
| [getResultSet()](#getResultSet) | Gibt das zugrunde liegende Java ResultSet-Objekt zurück. |
| [getRows()](#getRows) | Liefert die Sammlung der Zeilen, die zu dieser Tabelle gehören. |
| [getTableName()](#getTableName) | Liefert den Namen der [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [newRow()](#newRow) | Erstellt ein neues [DataRow](../../com.aspose.words.net.system.data/datarow/) mit demselben Schema wie die Tabelle. |
| [onDataColumnDeleted(System.Data.DataColumn column)](#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn) |  |
| [onDataColumnInserted(System.Data.DataColumn column)](#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn) |  |
| [onDataRowChanged(System.Data.DataRow row)](#onDataRowChanged-com.aspose.words.net.System.Data.DataRow) |  |
| [onDataRowDeleted(System.Data.DataRow row)](#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow) |  |
| [onDataRowInserted(System.Data.DataRow row)](#onDataRowInserted-com.aspose.words.net.System.Data.DataRow) |  |
| [refresh()](#refresh) | Lädt alle Daten aus dem ResultSet neu, falls es vorhanden ist. |
| [setEnforceConstraints(boolean enforceConstraints)](#setEnforceConstraints-boolean) |  |
| [setNamespace(String value)](#setNamespace-java.lang.String) | Setzt den Namensraum für die XML-Darstellung der in der [DataTable](../../com.aspose.words.net.system.data/datatable/) gespeicherten Daten. |
| [setPrimaryKey(System.Data.DataColumn[] value)](#setPrimaryKey-com.aspose.words.net.System.Data.DataColumn) | Setzt ein Array von Spalten, die als Primärschlüssel für die Datentabelle fungieren. |
| [setTableName(String value)](#setTableName-java.lang.String) | Setzt den Namen der [DataTable](../../com.aspose.words.net.system.data/datatable/). |
### DataTable() {#DataTable}
```
public DataTable()
```


Initialisiert eine neue Instanz der Klasse [DataTable](../../com.aspose.words.net.system.data/datatable/) ohne Argumente.

### DataTable(String tableName) {#DataTable-java.lang.String}
```
public DataTable(String tableName)
```


Initialisiert eine neue Instanz der Klasse [DataTable](../../com.aspose.words.net.system.data/datatable/) mit dem angegebenen Tabellennamen.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tableName | java.lang.String | Der Name, der der Tabelle zugewiesen werden soll. Wenn  tableName  null oder ein leerer String ist, wird beim Hinzufügen zur [DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/) ein Standardname vergeben. |

### DataTable(ResultSet resultSet) {#DataTable-java.sql.ResultSet}
```
public DataTable(ResultSet resultSet)
```


Erstellt ein Objekt, indem das angegebene ResultSet umschlossen wird. Versucht, den Tabellennamen aus den Metadaten der ersten Spalte des ResultSet zu ermitteln.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | Datensatz |

### DataTable(ResultSet resultSet, String tableName) {#DataTable-java.sql.ResultSet-java.lang.String}
```
public DataTable(ResultSet resultSet, String tableName)
```


Erstellt ein Objekt, indem das angegebene ResultSet umschlossen wird.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | Datensatz |
| tableName | java.lang.String | Name der Tabelle |

### acceptChanges() {#acceptChanges}
```
public void acceptChanges()
```


Übernimmt alle Änderungen, die an dieser Tabelle seit dem letzten Aufruf von [acceptChanges()](../../com.aspose.words.net.system.data/datatable/\#acceptChanges) vorgenommen wurden.

### addEventListener(System.Data.DataTableEventListener listener) {#addEventListener-com.aspose.words.net.System.Data.DataTableEventListener}
```
public synchronized void addEventListener(System.Data.DataTableEventListener listener)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| listener | [DataTableEventListener](../../com.aspose.words.net.system.data/datatableeventlistener/) |  |

### clearEventListneers() {#clearEventListneers}
```
public synchronized void clearEventListneers()
```




### close() {#close}
```
public void close()
```




### containsColumn(String columnName) {#containsColumn-java.lang.String}
```
public boolean containsColumn(String columnName)
```


Überprüfen, ob die angegebene Spalte existiert oder nicht

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| columnName | java.lang.String | Name der Spalte |

**Returns:**
boolean - `true` ist die Spalte, die durch den angegebenen `columnName` gefunden werden kann
### getChildRelations() {#getChildRelations}
```
public System.Data.DataRelationCollection getChildRelations()
```


Liefert die Sammlung der untergeordneten Beziehungen für diese [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains the child relations for the table. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getColumnName(int index) {#getColumnName-int}
```
public String getColumnName(int index)
```


Analog für .Net DataTable.Columns[i].ColumnName

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | \- Spaltenindex |

**Returns:**
java.lang.String - Spaltenname nach seinem Index.
### getColumns() {#getColumns}
```
public System.Data.DataColumnCollection getColumns()
```


Liefert die Sammlung der Spalten, die zu dieser Tabelle gehören.

**Returns:**
[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) - A [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) that contains the collection of [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects for the table. An empty collection is returned if no [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects exist.
### getColumnsCount() {#getColumnsCount}
```
public int getColumnsCount()
```




**Returns:**
int - Spaltenanzahl
### getConstraints() {#getConstraints}
```
public System.Data.ConstraintCollection getConstraints()
```


Liefert die Sammlung der von dieser Tabelle verwalteten Einschränkungen.

**Returns:**
[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) - A [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) that contains the collection of [Constraint](../../com.aspose.words.net.system.data/constraint/) objects for the table. An empty collection is returned if no [Constraint](../../com.aspose.words.net.system.data/constraint/) objects exist.
### getDataSet() {#getDataSet}
```
public System.Data.DataSet getDataSet()
```


Liefert das [DataSet](../../com.aspose.words.net.system.data/dataset/), zu dem diese Tabelle gehört.

**Returns:**
[DataSet](../../com.aspose.words.net.system.data/dataset/) - The [DataSet](../../com.aspose.words.net.system.data/dataset/) to which this table belongs.
### getEnforceConstraints() {#getEnforceConstraints}
```
public boolean getEnforceConstraints()
```




**Returns:**
boolean - Flag, das anzeigt, ob eine Check-Constraint-Verletzung vorliegt oder nicht
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


Liefert den Namensraum für die XML-Darstellung der in der [DataTable](../../com.aspose.words.net.system.data/datatable/) gespeicherten Daten.

**Returns:**
java.lang.String - Der Namensraum der [DataTable](../../com.aspose.words.net.system.data/datatable/).
### getParentRelations() {#getParentRelations}
```
public System.Data.DataRelationCollection getParentRelations()
```


Liefert die Sammlung der übergeordneten Beziehungen für diese [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains the parent relations for the table. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getPrimaryKey() {#getPrimaryKey}
```
public System.Data.DataColumn[] getPrimaryKey()
```


Liefert ein Array von Spalten, die als Primärschlüssel für die Datentabelle fungieren.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Ein Array von [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten.
### getResultSet() {#getResultSet}
```
public ResultSet getResultSet()
```


Gibt das zugrunde liegende Java ResultSet-Objekt zurück. Idealerweise möchten wir mit DataTable auf .Net-Art arbeiten. Aber einige Benutzer und sogar einige unserer Beispielcodes verwenden diese Eigenschaft.

**Returns:**
java.sql.ResultSet - das zugrunde liegende java.sql.ResultSet
### getRows() {#getRows}
```
public System.Data.DataRowCollection getRows()
```


Liefert die Sammlung der Zeilen, die zu dieser Tabelle gehören.

**Returns:**
[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) - A [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) that contains [DataRow](../../com.aspose.words.net.system.data/datarow/) objects; otherwise a null value if no [DataRow](../../com.aspose.words.net.system.data/datarow/) objects exist.
### getTableName() {#getTableName}
```
public String getTableName()
```


Liefert den Namen der [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
java.lang.String - Der Name der [DataTable](../../com.aspose.words.net.system.data/datatable/).
### newRow() {#newRow}
```
public System.Data.DataRow newRow()
```


Erstellt ein neues [DataRow](../../com.aspose.words.net.system.data/datarow/) mit demselben Schema wie die Tabelle.

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A [DataRow](../../com.aspose.words.net.system.data/datarow/) with the same schema as the [DataTable](../../com.aspose.words.net.system.data/datatable/).
### onDataColumnDeleted(System.Data.DataColumn column) {#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn}
```
public void onDataColumnDeleted(System.Data.DataColumn column)
```


Listener aktualisieren, wenn DataColumn gelöscht wird

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) |  |

### onDataColumnInserted(System.Data.DataColumn column) {#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn}
```
public void onDataColumnInserted(System.Data.DataColumn column)
```


Listener aktualisieren, wenn DataColumn eingefügt wird

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) |  |

### onDataRowChanged(System.Data.DataRow row) {#onDataRowChanged-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowChanged(System.Data.DataRow row)
```


Listener aktualisieren, wenn DataRow geändert wird

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### onDataRowDeleted(System.Data.DataRow row) {#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowDeleted(System.Data.DataRow row)
```


Listener aktualisieren, wenn DataRow gelöscht wird

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### onDataRowInserted(System.Data.DataRow row) {#onDataRowInserted-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowInserted(System.Data.DataRow row)
```


Listener aktualisieren, wenn DataRow eingefügt wird

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### refresh() {#refresh}
```
public void refresh()
```


Lädt alle Daten aus dem ResultSet neu, falls es vorhanden ist.

### setEnforceConstraints(boolean enforceConstraints) {#setEnforceConstraints-boolean}
```
public void setEnforceConstraints(boolean enforceConstraints)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| enforceConstraints | boolean | ist das Flag, das anzeigt, ob eine Check-Constraint-Verletzung vorliegt oder nicht |

### setNamespace(String value) {#setNamespace-java.lang.String}
```
public void setNamespace(String value)
```


Setzt den Namensraum für die XML-Darstellung der in der [DataTable](../../com.aspose.words.net.system.data/datatable/) gespeicherten Daten.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | java.lang.String | Der Namensraum der [DataTable](../../com.aspose.words.net.system.data/datatable/). |

### setPrimaryKey(System.Data.DataColumn[] value) {#setPrimaryKey-com.aspose.words.net.System.Data.DataColumn}
```
public void setPrimaryKey(System.Data.DataColumn[] value)
```


Setzt ein Array von Spalten, die als Primärschlüssel für die Datentabelle fungieren.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Ein Array von [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten. |

### setTableName(String value) {#setTableName-java.lang.String}
```
public void setTableName(String value)
```


Setzt den Namen der [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | java.lang.String | Der Name der [DataTable](../../com.aspose.words.net.system.data/datatable/). |

