---
title: "DataRow"
linktitle: "DataRow"
second_title: "Aspose.Words für Java"
description: "Stellt eine Datenzeile in einer DataTable in Java dar."
type: docs
weight: 20
url: /de/java/com.aspose.words.net.system.data/datarow/
---

**Inheritance:**
java.lang.Object
```
public class DataRow
```

Stellt eine Datenzeile in einer [DataTable](../../com.aspose.words.net.system.data/datatable/) dar.
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [delete()](#delete) | Löscht die [DataRow](../../com.aspose.words.net.system.data/datarow/). |
| [get(System.Data.DataColumn column)](#get-com.aspose.words.net.System.Data.DataColumn) | Ruft die in der angegebenen [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) gespeicherten Daten ab. |
| [get(int columnIndex)](#get-int) | Ruft die in der durch Index angegebenen Spalte gespeicherten Daten ab. |
| [get(String columnName)](#get-java.lang.String) | Ruft die in der durch Namen angegebenen Spalte gespeicherten Daten ab. |
| [getChildRows(System.Data.DataRelation relation)](#getChildRows-com.aspose.words.net.System.Data.DataRelation) | Ruft die untergeordneten Zeilen dieses [DataRow](../../com.aspose.words.net.system.data/datarow/) unter Verwendung der angegebenen [DataRelation](../../com.aspose.words.net.system.data/datarelation/) ab. |
| [getItemArray()](#getItemArray) | Ruft alle Werte für diese Zeile über ein Array ab. |
| [getKeyValues(System.Data.DataKey childKey)](#getKeyValues-com.aspose.words.net.System.Data.DataKey) |  |
| [getOriginalValue(String columnName)](#getOriginalValue-java.lang.String) |  |
| [getParentRow(System.Data.DataRelation relation)](#getParentRow-com.aspose.words.net.System.Data.DataRelation) | Ruft die übergeordnete Zeile eines [DataRow](../../com.aspose.words.net.system.data/datarow/) unter Verwendung der angegebenen [DataRelation](../../com.aspose.words.net.system.data/datarelation/) ab. |
| [getParentRows(System.Data.DataRelation relation)](#getParentRows-com.aspose.words.net.System.Data.DataRelation) | Ruft die übergeordneten Zeilen eines [DataRow](../../com.aspose.words.net.system.data/datarow/) unter Verwendung der angegebenen [DataRelation](../../com.aspose.words.net.system.data/datarelation/) ab. |
| [getRowState()](#getRowState) | Ruft den aktuellen Zustand der Zeile in Bezug auf ihre Beziehung zur [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) ab. |
| [getTable()](#getTable) | Ruft die [DataTable](../../com.aspose.words.net.system.data/datatable/) ab, für die diese Zeile ein Schema hat. |
| [readFrom(ResultSet resultSet)](#readFrom-java.sql.ResultSet) | Liest Werte aus dem java.sql.ResultSet |
| [remove(int index)](#remove-int) |  |
| [set(System.Data.DataColumn column, Object value)](#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object) | Setzt die in der angegebenen [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) gespeicherten Daten. |
| [set(int columnIndex, Object value)](#set-int-java.lang.Object) | Setzt die in der durch Index angegebenen Spalte gespeicherten Daten. |
| [set(String columnName, Object value)](#set-java.lang.String-java.lang.Object) | Setzt die in der durch Namen angegebenen Spalte gespeicherten Daten. |
| [setItemArray(Object[] value)](#setItemArray-java.lang.Object) | Setzt alle Werte für diese Zeile über ein Array. |
| [setOriginalValue(String columnName, Object data)](#setOriginalValue-java.lang.String-java.lang.Object) |  |
| [setRowState(int state)](#setRowState-int) |  |
| [toString()](#toString) |  |
### delete() {#delete}
```
public void delete()
```


Löscht die [DataRow](../../com.aspose.words.net.system.data/datarow/).

### get(System.Data.DataColumn column) {#get-com.aspose.words.net.System.Data.DataColumn}
```
public Object get(System.Data.DataColumn column)
```


Ruft die in der angegebenen [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) gespeicherten Daten ab.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Eine [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) die die Daten enthält. |

**Returns:**
java.lang.Object - Ein java.lang.Object, das die Daten enthält.
### get(int columnIndex) {#get-int}
```
public Object get(int columnIndex)
```


Ruft die in der durch Index angegebenen Spalte gespeicherten Daten ab.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| columnIndex | int | Der nullbasierte Index der Spalte. |

**Returns:**
java.lang.Object - Ein java.lang.Object, das die Daten enthält.
### get(String columnName) {#get-java.lang.String}
```
public Object get(String columnName)
```


Ruft die in der durch Namen angegebenen Spalte gespeicherten Daten ab.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| columnName | java.lang.String | Der Name der Spalte. |

**Returns:**
java.lang.Object - Ein java.lang.Object, das die Daten enthält.
### getChildRows(System.Data.DataRelation relation) {#getChildRows-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow[] getChildRows(System.Data.DataRelation relation)
```


Ruft die untergeordneten Zeilen dieses [DataRow](../../com.aspose.words.net.system.data/datarow/) unter Verwendung der angegebenen [DataRelation](../../com.aspose.words.net.system.data/datarelation/) ab.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | Die zu verwendende [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |

**Returns:**
com.aspose.words.net.System.Data.DataRow[] - Ein Array von [DataRow](../../com.aspose.words.net.system.data/datarow/) Objekten oder ein Array der Länge null.
### getItemArray() {#getItemArray}
```
public Object[] getItemArray()
```


Ruft alle Werte für diese Zeile über ein Array ab.

**Returns:**
java.lang.Object[] - Ein Array vom Typ java.lang.Object.
### getKeyValues(System.Data.DataKey childKey) {#getKeyValues-com.aspose.words.net.System.Data.DataKey}
```
public Object[] getKeyValues(System.Data.DataKey childKey)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| childKey | [DataKey](../../com.aspose.words.net.system.data/datakey/) |  |

**Returns:**
java.lang.Object[]
### getOriginalValue(String columnName) {#getOriginalValue-java.lang.String}
```
public Object getOriginalValue(String columnName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| columnName | java.lang.String |  |

**Returns:**
java.lang.Object
### getParentRow(System.Data.DataRelation relation) {#getParentRow-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow getParentRow(System.Data.DataRelation relation)
```


Ruft die übergeordnete Zeile eines [DataRow](../../com.aspose.words.net.system.data/datarow/) unter Verwendung der angegebenen [DataRelation](../../com.aspose.words.net.system.data/datarelation/) ab.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | Die zu verwendende [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - The parent [DataRow](../../com.aspose.words.net.system.data/datarow/) of the current row.
### getParentRows(System.Data.DataRelation relation) {#getParentRows-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow[] getParentRows(System.Data.DataRelation relation)
```


Ruft die übergeordneten Zeilen eines [DataRow](../../com.aspose.words.net.system.data/datarow/) unter Verwendung der angegebenen [DataRelation](../../com.aspose.words.net.system.data/datarelation/) ab.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | Die zu verwendende [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |

**Returns:**
com.aspose.words.net.System.Data.DataRow[] - Ein Array von [DataRow](../../com.aspose.words.net.system.data/datarow/) Objekten oder ein Array der Länge null.
### getRowState() {#getRowState}
```
public int getRowState()
```


Ruft den aktuellen Zustand der Zeile in Bezug auf ihre Beziehung zur [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) ab.

**Returns:**
int - Einer der [DataRowState](../../com.aspose.words.net.system.data/datarowstate/) Werte. Der zurückgegebene Wert ist eine bitweise Kombination der [DataRowState](../../com.aspose.words.net.system.data/datarowstate/) Konstanten.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Ruft die [DataTable](../../com.aspose.words.net.system.data/datatable/) ab, für die diese Zeile ein Schema hat.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) to which this row belongs.
### readFrom(ResultSet resultSet) {#readFrom-java.sql.ResultSet}
```
public boolean readFrom(ResultSet resultSet)
```


Liest Werte aus dem java.sql.ResultSet

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | Speicher zum Lesen von |

**Returns:**
boolean - true, wenn keine Lesefehler aufgetreten sind
### remove(int index) {#remove-int}
```
public void remove(int index)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int |  |

### set(System.Data.DataColumn column, Object value) {#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object}
```
public void set(System.Data.DataColumn column, Object value)
```


Setzt die in der angegebenen [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) gespeicherten Daten.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Eine [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) die die Daten enthält. |
| Wert | java.lang.Object | Ein java.lang.Object, das die Daten enthält. |

### set(int columnIndex, Object value) {#set-int-java.lang.Object}
```
public void set(int columnIndex, Object value)
```


Setzt die in der durch Index angegebenen Spalte gespeicherten Daten.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| columnIndex | int | Der nullbasierte Index der Spalte. |
| Wert | java.lang.Object | Ein java.lang.Object, das die Daten enthält. |

### set(String columnName, Object value) {#set-java.lang.String-java.lang.Object}
```
public void set(String columnName, Object value)
```


Setzt die in der durch Namen angegebenen Spalte gespeicherten Daten.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| columnName | java.lang.String | Der Name der Spalte. |
| Wert | java.lang.Object | Ein java.lang.Object, das die Daten enthält. |

### setItemArray(Object[] value) {#setItemArray-java.lang.Object}
```
public void setItemArray(Object[] value)
```


Setzt alle Werte für diese Zeile über ein Array.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.Object[] | Ein Array vom Typ java.lang.Object. |

### setOriginalValue(String columnName, Object data) {#setOriginalValue-java.lang.String-java.lang.Object}
```
public void setOriginalValue(String columnName, Object data)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| columnName | java.lang.String |  |
| Daten | java.lang.Object |  |

### setRowState(int state) {#setRowState-int}
```
public void setRowState(int state)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Zustand | int |  |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
