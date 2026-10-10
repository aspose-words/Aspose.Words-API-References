---
title: "DataRow"
linktitle: "DataRow"
second_title: "Aspose.Words para Java"
description: "Representa una fila de datos en un DataTable en Java."
type: docs
weight: 20
url: /es/java/com.aspose.words.net.system.data/datarow/
---

**Inheritance:**
java.lang.Object
```
public class DataRow
```

Representa una fila de datos en un [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Métodos

| Método | Descripción |
| --- | --- |
| [delete()](#delete) | Elimina el [DataRow](../../com.aspose.words.net.system.data/datarow/). |
| [get(System.Data.DataColumn column)](#get-com.aspose.words.net.System.Data.DataColumn) | Obtiene los datos almacenados en el [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) especificado. |
| [get(int columnIndex)](#get-int) | Obtiene los datos almacenados en la columna especificada por índice. |
| [get(String columnName)](#get-java.lang.String) | Obtiene los datos almacenados en la columna especificada por nombre. |
| [getChildRows(System.Data.DataRelation relation)](#getChildRows-com.aspose.words.net.System.Data.DataRelation) | Obtiene las filas hijas de este [DataRow](../../com.aspose.words.net.system.data/datarow/) usando la [DataRelation](../../com.aspose.words.net.system.data/datarelation/) especificada. |
| [getItemArray()](#getItemArray) | Obtiene todos los valores de esta fila mediante una matriz. |
| [getKeyValues(System.Data.DataKey childKey)](#getKeyValues-com.aspose.words.net.System.Data.DataKey) |  |
| [getOriginalValue(String columnName)](#getOriginalValue-java.lang.String) |  |
| [getParentRow(System.Data.DataRelation relation)](#getParentRow-com.aspose.words.net.System.Data.DataRelation) | Obtiene la fila padre de un [DataRow](../../com.aspose.words.net.system.data/datarow/) usando la [DataRelation](../../com.aspose.words.net.system.data/datarelation/) especificada. |
| [getParentRows(System.Data.DataRelation relation)](#getParentRows-com.aspose.words.net.System.Data.DataRelation) | Obtiene las filas padre de un [DataRow](../../com.aspose.words.net.system.data/datarow/) usando la [DataRelation](../../com.aspose.words.net.system.data/datarelation/) especificada. |
| [getRowState()](#getRowState) | Obtiene el estado actual de la fila con respecto a su relación con la [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/). |
| [getTable()](#getTable) | Obtiene el [DataTable](../../com.aspose.words.net.system.data/datatable/) para el cual esta fila tiene un esquema. |
| [readFrom(ResultSet resultSet)](#readFrom-java.sql.ResultSet) | Lee valores del java.sql.ResultSet |
| [remove(int index)](#remove-int) |  |
| [set(System.Data.DataColumn column, Object value)](#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object) | Establece los datos almacenados en el [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) especificado. |
| [set(int columnIndex, Object value)](#set-int-java.lang.Object) | Establece los datos almacenados en la columna especificada por índice. |
| [set(String columnName, Object value)](#set-java.lang.String-java.lang.Object) | Establece los datos almacenados en la columna especificada por nombre. |
| [setItemArray(Object[] value)](#setItemArray-java.lang.Object) | Establece todos los valores de esta fila mediante una matriz. |
| [setOriginalValue(String columnName, Object data)](#setOriginalValue-java.lang.String-java.lang.Object) |  |
| [setRowState(int state)](#setRowState-int) |  |
| [toString()](#toString) |  |
### delete() {#delete}
```
public void delete()
```


Elimina el [DataRow](../../com.aspose.words.net.system.data/datarow/).

### get(System.Data.DataColumn column) {#get-com.aspose.words.net.System.Data.DataColumn}
```
public Object get(System.Data.DataColumn column)
```


Obtiene los datos almacenados en el [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Un [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) que contiene los datos. |

**Returns:**
java.lang.Object - Un java.lang.Object que contiene los datos.
### get(int columnIndex) {#get-int}
```
public Object get(int columnIndex)
```


Obtiene los datos almacenados en la columna especificada por índice.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| columnIndex | int | El índice basado en cero de la columna. |

**Returns:**
java.lang.Object - Un java.lang.Object que contiene los datos.
### get(String columnName) {#get-java.lang.String}
```
public Object get(String columnName)
```


Obtiene los datos almacenados en la columna especificada por nombre.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| columnName | java.lang.String | El nombre de la columna. |

**Returns:**
java.lang.Object - Un java.lang.Object que contiene los datos.
### getChildRows(System.Data.DataRelation relation) {#getChildRows-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow[] getChildRows(System.Data.DataRelation relation)
```


Obtiene las filas hijas de este [DataRow](../../com.aspose.words.net.system.data/datarow/) usando la [DataRelation](../../com.aspose.words.net.system.data/datarelation/) especificada.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | La [DataRelation](../../com.aspose.words.net.system.data/datarelation/) a usar. |

**Returns:**
com.aspose.words.net.System.Data.DataRow[] - Una matriz de objetos [DataRow](../../com.aspose.words.net.system.data/datarow/) o una matriz de longitud cero.
### getItemArray() {#getItemArray}
```
public Object[] getItemArray()
```


Obtiene todos los valores de esta fila mediante una matriz.

**Returns:**
java.lang.Object[] - Una matriz del tipo java.lang.Object.
### getKeyValues(System.Data.DataKey childKey) {#getKeyValues-com.aspose.words.net.System.Data.DataKey}
```
public Object[] getKeyValues(System.Data.DataKey childKey)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| childKey | [DataKey](../../com.aspose.words.net.system.data/datakey/) |  |

**Returns:**
java.lang.Object[]
### getOriginalValue(String columnName) {#getOriginalValue-java.lang.String}
```
public Object getOriginalValue(String columnName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| columnName | java.lang.String |  |

**Returns:**
java.lang.Object
### getParentRow(System.Data.DataRelation relation) {#getParentRow-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow getParentRow(System.Data.DataRelation relation)
```


Obtiene la fila padre de un [DataRow](../../com.aspose.words.net.system.data/datarow/) usando la [DataRelation](../../com.aspose.words.net.system.data/datarelation/) especificada.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | La [DataRelation](../../com.aspose.words.net.system.data/datarelation/) a usar. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - The parent [DataRow](../../com.aspose.words.net.system.data/datarow/) of the current row.
### getParentRows(System.Data.DataRelation relation) {#getParentRows-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow[] getParentRows(System.Data.DataRelation relation)
```


Obtiene las filas padre de un [DataRow](../../com.aspose.words.net.system.data/datarow/) usando la [DataRelation](../../com.aspose.words.net.system.data/datarelation/) especificada.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | La [DataRelation](../../com.aspose.words.net.system.data/datarelation/) a usar. |

**Returns:**
com.aspose.words.net.System.Data.DataRow[] - Una matriz de objetos [DataRow](../../com.aspose.words.net.system.data/datarow/) o una matriz de longitud cero.
### getRowState() {#getRowState}
```
public int getRowState()
```


Obtiene el estado actual de la fila con respecto a su relación con la [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).

**Returns:**
int - Uno de los valores de [DataRowState](../../com.aspose.words.net.system.data/datarowstate/). El valor devuelto es una combinación bit a bit de las constantes de [DataRowState](../../com.aspose.words.net.system.data/datarowstate/).
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Obtiene el [DataTable](../../com.aspose.words.net.system.data/datatable/) para el cual esta fila tiene un esquema.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) to which this row belongs.
### readFrom(ResultSet resultSet) {#readFrom-java.sql.ResultSet}
```
public boolean readFrom(ResultSet resultSet)
```


Lee valores del java.sql.ResultSet

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | almacenamiento para leer |

**Returns:**
boolean - verdadero si no se produjeron errores de lectura
### remove(int index) {#remove-int}
```
public void remove(int index)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |

### set(System.Data.DataColumn column, Object value) {#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object}
```
public void set(System.Data.DataColumn column, Object value)
```


Establece los datos almacenados en el [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Un [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) que contiene los datos. |
| valor | java.lang.Object | Un java.lang.Object que contiene los datos. |

### set(int columnIndex, Object value) {#set-int-java.lang.Object}
```
public void set(int columnIndex, Object value)
```


Establece los datos almacenados en la columna especificada por índice.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| columnIndex | int | El índice basado en cero de la columna. |
| valor | java.lang.Object | Un java.lang.Object que contiene los datos. |

### set(String columnName, Object value) {#set-java.lang.String-java.lang.Object}
```
public void set(String columnName, Object value)
```


Establece los datos almacenados en la columna especificada por nombre.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| columnName | java.lang.String | El nombre de la columna. |
| valor | java.lang.Object | Un java.lang.Object que contiene los datos. |

### setItemArray(Object[] value) {#setItemArray-java.lang.Object}
```
public void setItemArray(Object[] value)
```


Establece todos los valores de esta fila mediante una matriz.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.Object[] | Una matriz del tipo java.lang.Object. |

### setOriginalValue(String columnName, Object data) {#setOriginalValue-java.lang.String-java.lang.Object}
```
public void setOriginalValue(String columnName, Object data)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| columnName | java.lang.String |  |
| datos | java.lang.Object |  |

### setRowState(int state) {#setRowState-int}
```
public void setRowState(int state)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| estado | int |  |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
