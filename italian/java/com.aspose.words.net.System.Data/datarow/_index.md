---
title: "DataRow"
linktitle: "DataRow"
second_title: "Aspose.Words per Java"
description: "Rappresenta una riga di dati in un DataTable in Java."
type: docs
weight: 20
url: /it/java/com.aspose.words.net.system.data/datarow/
---

**Inheritance:**
java.lang.Object
```
public class DataRow
```

Rappresenta una riga di dati in un [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [delete()](#delete) | Elimina il [DataRow](../../com.aspose.words.net.system.data/datarow/). |
| [get(System.Data.DataColumn column)](#get-com.aspose.words.net.System.Data.DataColumn) | Ottiene i dati memorizzati nella [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [get(int columnIndex)](#get-int) | Ottiene i dati memorizzati nella colonna specificata per indice. |
| [get(String columnName)](#get-java.lang.String) | Ottiene i dati memorizzati nella colonna specificata per nome. |
| [getChildRows(System.Data.DataRelation relation)](#getChildRows-com.aspose.words.net.System.Data.DataRelation) | Ottiene le righe figlie di questo [DataRow](../../com.aspose.words.net.system.data/datarow/) utilizzando la [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getItemArray()](#getItemArray) | Ottiene tutti i valori per questa riga tramite un array. |
| [getKeyValues(System.Data.DataKey childKey)](#getKeyValues-com.aspose.words.net.System.Data.DataKey) |  |
| [getOriginalValue(String columnName)](#getOriginalValue-java.lang.String) |  |
| [getParentRow(System.Data.DataRelation relation)](#getParentRow-com.aspose.words.net.System.Data.DataRelation) | Ottiene la riga padre di un [DataRow](../../com.aspose.words.net.system.data/datarow/) utilizzando la [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getParentRows(System.Data.DataRelation relation)](#getParentRows-com.aspose.words.net.System.Data.DataRelation) | Ottiene le righe padre di un [DataRow](../../com.aspose.words.net.system.data/datarow/) utilizzando la [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getRowState()](#getRowState) | Ottiene lo stato corrente della riga rispetto alla sua relazione con la [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/). |
| [getTable()](#getTable) | Ottiene il [DataTable](../../com.aspose.words.net.system.data/datatable/) per il quale questa riga ha uno schema. |
| [readFrom(ResultSet resultSet)](#readFrom-java.sql.ResultSet) | Legge i valori dal java.sql.ResultSet |
| [remove(int index)](#remove-int) |  |
| [set(System.Data.DataColumn column, Object value)](#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object) | Imposta i dati memorizzati nella [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [set(int columnIndex, Object value)](#set-int-java.lang.Object) | Imposta i dati memorizzati nella colonna specificata per indice. |
| [set(String columnName, Object value)](#set-java.lang.String-java.lang.Object) | Imposta i dati memorizzati nella colonna specificata per nome. |
| [setItemArray(Object[] value)](#setItemArray-java.lang.Object) | Imposta tutti i valori per questa riga tramite un array. |
| [setOriginalValue(String columnName, Object data)](#setOriginalValue-java.lang.String-java.lang.Object) |  |
| [setRowState(int state)](#setRowState-int) |  |
| [toString()](#toString) |  |
### delete() {#delete}
```
public void delete()
```


Elimina il [DataRow](../../com.aspose.words.net.system.data/datarow/).

### get(System.Data.DataColumn column) {#get-com.aspose.words.net.System.Data.DataColumn}
```
public Object get(System.Data.DataColumn column)
```


Ottiene i dati memorizzati nella [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Una [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) che contiene i dati. |

**Returns:**
java.lang.Object - Un java.lang.Object che contiene i dati.
### get(int columnIndex) {#get-int}
```
public Object get(int columnIndex)
```


Ottiene i dati memorizzati nella colonna specificata per indice.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| columnIndex | int | L'indice basato su zero della colonna. |

**Returns:**
java.lang.Object - Un java.lang.Object che contiene i dati.
### get(String columnName) {#get-java.lang.String}
```
public Object get(String columnName)
```


Ottiene i dati memorizzati nella colonna specificata per nome.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| columnName | java.lang.String | Il nome della colonna. |

**Returns:**
java.lang.Object - Un java.lang.Object che contiene i dati.
### getChildRows(System.Data.DataRelation relation) {#getChildRows-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow[] getChildRows(System.Data.DataRelation relation)
```


Ottiene le righe figlie di questo [DataRow](../../com.aspose.words.net.system.data/datarow/) utilizzando la [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | La [DataRelation](../../com.aspose.words.net.system.data/datarelation/) da utilizzare. |

**Returns:**
com.aspose.words.net.System.Data.DataRow[] - Un array di oggetti [DataRow](../../com.aspose.words.net.system.data/datarow/) o un array di lunghezza zero.
### getItemArray() {#getItemArray}
```
public Object[] getItemArray()
```


Ottiene tutti i valori per questa riga tramite un array.

**Returns:**
java.lang.Object[] - Un array di tipo java.lang.Object.
### getKeyValues(System.Data.DataKey childKey) {#getKeyValues-com.aspose.words.net.System.Data.DataKey}
```
public Object[] getKeyValues(System.Data.DataKey childKey)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| childKey | [DataKey](../../com.aspose.words.net.system.data/datakey/) |  |

**Returns:**
java.lang.Object[]
### getOriginalValue(String columnName) {#getOriginalValue-java.lang.String}
```
public Object getOriginalValue(String columnName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| columnName | java.lang.String |  |

**Returns:**
java.lang.Object
### getParentRow(System.Data.DataRelation relation) {#getParentRow-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow getParentRow(System.Data.DataRelation relation)
```


Ottiene la riga padre di un [DataRow](../../com.aspose.words.net.system.data/datarow/) utilizzando la [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | La [DataRelation](../../com.aspose.words.net.system.data/datarelation/) da utilizzare. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - The parent [DataRow](../../com.aspose.words.net.system.data/datarow/) of the current row.
### getParentRows(System.Data.DataRelation relation) {#getParentRows-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow[] getParentRows(System.Data.DataRelation relation)
```


Ottiene le righe padre di un [DataRow](../../com.aspose.words.net.system.data/datarow/) utilizzando la [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | La [DataRelation](../../com.aspose.words.net.system.data/datarelation/) da utilizzare. |

**Returns:**
com.aspose.words.net.System.Data.DataRow[] - Un array di oggetti [DataRow](../../com.aspose.words.net.system.data/datarow/) o un array di lunghezza zero.
### getRowState() {#getRowState}
```
public int getRowState()
```


Ottiene lo stato corrente della riga rispetto alla sua relazione con la [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).

**Returns:**
int - Uno dei valori di [DataRowState](../../com.aspose.words.net.system.data/datarowstate/) . Il valore restituito è una combinazione bitwise dei costanti di [DataRowState](../../com.aspose.words.net.system.data/datarowstate/).
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Ottiene il [DataTable](../../com.aspose.words.net.system.data/datatable/) per il quale questa riga ha uno schema.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) to which this row belongs.
### readFrom(ResultSet resultSet) {#readFrom-java.sql.ResultSet}
```
public boolean readFrom(ResultSet resultSet)
```


Legge i valori dal java.sql.ResultSet

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | archivio da cui leggere |

**Returns:**
boolean - true se non si sono verificati errori di lettura
### remove(int index) {#remove-int}
```
public void remove(int index)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int |  |

### set(System.Data.DataColumn column, Object value) {#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object}
```
public void set(System.Data.DataColumn column, Object value)
```


Imposta i dati memorizzati nella [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Una [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) che contiene i dati. |
| valore | java.lang.Object | Un java.lang.Object che contiene i dati. |

### set(int columnIndex, Object value) {#set-int-java.lang.Object}
```
public void set(int columnIndex, Object value)
```


Imposta i dati memorizzati nella colonna specificata per indice.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| columnIndex | int | L'indice basato su zero della colonna. |
| valore | java.lang.Object | Un java.lang.Object che contiene i dati. |

### set(String columnName, Object value) {#set-java.lang.String-java.lang.Object}
```
public void set(String columnName, Object value)
```


Imposta i dati memorizzati nella colonna specificata per nome.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| columnName | java.lang.String | Il nome della colonna. |
| valore | java.lang.Object | Un java.lang.Object che contiene i dati. |

### setItemArray(Object[] value) {#setItemArray-java.lang.Object}
```
public void setItemArray(Object[] value)
```


Imposta tutti i valori per questa riga tramite un array.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.Object[] | Un array di tipo java.lang.Object. |

### setOriginalValue(String columnName, Object data) {#setOriginalValue-java.lang.String-java.lang.Object}
```
public void setOriginalValue(String columnName, Object data)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| columnName | java.lang.String |  |
| dati | java.lang.Object |  |

### setRowState(int state) {#setRowState-int}
```
public void setRowState(int state)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stato | int |  |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
