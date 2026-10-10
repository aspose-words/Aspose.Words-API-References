---
title: "DataTableReader"
linktitle: "DataTableReader"
second_title: "Aspose.Words para Java"
description: "El DataTableReader obtiene el contenido de uno o más objetos DataTable en forma de uno o más conjuntos de resultados de solo lectura y solo avance en Java."
type: docs
weight: 27
url: /es/java/com.aspose.words.net.system.data/datatablereader/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Common.DbDataReader](../../com.aspose.words.net.system.data.common/dbdatareader/)
```
public class DataTableReader extends System.Data.Common.DbDataReader
```

El [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) obtiene el contenido de uno o más objetos [DataTable](../../com.aspose.words.net.system.data/datatable/) en forma de uno o más conjuntos de resultados de solo lectura y solo avance.
## Constructores

| Constructor | Descripción |
| --- | --- |
| [DataTableReader(System.Data.DataTable dataTable)](#DataTableReader-com.aspose.words.net.System.Data.DataTable) | Inicializa una nueva instancia de la clase [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) usando datos de la [DataTable](../../com.aspose.words.net.system.data/datatable/) proporcionada. |
| [DataTableReader(System.Data.DataTable[] dataTables)](#DataTableReader-com.aspose.words.net.System.Data.DataTable) | Inicializa una nueva instancia de la clase [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) usando la matriz proporcionada de objetos [DataTable](../../com.aspose.words.net.system.data/datatable/). |
## Métodos

| Método | Descripción |
| --- | --- |
| [close()](#close) | Cierra el [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) actual. |
| [get(int ordinal)](#get-int) | Obtiene el valor de la columna especificada en su formato nativo dado el ordinal de la columna. |
| [get(String name)](#get-java.lang.String) | Obtiene el valor de la columna especificada en su formato nativo dado el nombre de la columna. |
| [getDepth()](#getDepth) | La profundidad de anidamiento para la fila actual del [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/). |
| [getFieldCount()](#getFieldCount) | Devuelve el número de columnas en la fila actual. |
| [getFieldType(int ordinal)](#getFieldType-int) | Obtiene el java.lang.Class que es el tipo de datos del objeto. |
| [getName(int ordinal)](#getName-int) | Obtiene el valor de la columna especificada como un java.lang.String. |
| [getRecordsAffected()](#getRecordsAffected) | Obtiene el número de filas insertadas, modificadas o eliminadas por la ejecución de la instrucción SQL. |
| [getSchemaTable()](#getSchemaTable) | Devuelve un [DataTable](../../com.aspose.words.net.system.data/datatable/) que describe los metadatos de columna del [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/). |
| [getValue(int ordinal)](#getValue-int) | Obtiene el valor de la columna especificada en su formato nativo. |
| [hasRows()](#hasRows) | Obtiene un valor que indica si el [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) contiene una o más filas. |
| [isClosed()](#isClosed) | Obtiene un valor que indica si el [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) está cerrado. |
| [iterator()](#iterator) | Devuelve un enumerador que puede usarse para iterar a través de la colección de elementos. |
| [nextResult()](#nextResult) | Avanza el [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) al siguiente conjunto de resultados, si lo hay. |
| [read()](#read) | Avanza el [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) al siguiente registro. |
### DataTableReader(System.Data.DataTable dataTable) {#DataTableReader-com.aspose.words.net.System.Data.DataTable}
```
public DataTableReader(System.Data.DataTable dataTable)
```


Inicializa una nueva instancia de la clase [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) usando datos de la [DataTable](../../com.aspose.words.net.system.data/datatable/) proporcionada.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | El [DataTable](../../com.aspose.words.net.system.data/datatable/) del cual el nuevo [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) obtiene su conjunto de resultados. |

### DataTableReader(System.Data.DataTable[] dataTables) {#DataTableReader-com.aspose.words.net.System.Data.DataTable}
```
public DataTableReader(System.Data.DataTable[] dataTables)
```


Inicializa una nueva instancia de la clase [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) usando la matriz proporcionada de objetos [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| dataTables | [DataTable\[\]](../../com.aspose.words.net.system.data/datatable/) | La matriz de objetos [DataTable](../../com.aspose.words.net.system.data/datatable/) que suministra los resultados para el nuevo objeto [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/). |

### close() {#close}
```
public void close()
```


Cierra el [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) actual.

### get(int ordinal) {#get-int}
```
public Object get(int ordinal)
```


Obtiene el valor de la columna especificada en su formato nativo dado el ordinal de la columna.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| ordinal | int | El ordinal de columna basado en cero. |

**Returns:**
java.lang.Object - El valor de la columna especificada en su formato nativo.
### get(String name) {#get-java.lang.String}
```
public Object get(String name)
```


Obtiene el valor de la columna especificada en su formato nativo dado el nombre de la columna.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre de la columna. |

**Returns:**
java.lang.Object - El valor de la columna especificada en su formato nativo.
### getDepth() {#getDepth}
```
public int getDepth()
```


La profundidad de anidamiento para la fila actual del [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/).

**Returns:**
int - La profundidad de anidamiento para la fila actual; siempre cero.
### getFieldCount() {#getFieldCount}
```
public int getFieldCount()
```


Devuelve el número de columnas en la fila actual.

**Returns:**
int - Cuando no está posicionado en un conjunto de resultados válido, 0; de lo contrario, el número de columnas en la fila actual.
### getFieldType(int ordinal) {#getFieldType-int}
```
public Class getFieldType(int ordinal)
```


Obtiene el java.lang.Class que es el tipo de datos del objeto.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| ordinal | int | El ordinal de columna basado en cero. |

**Returns:**
java.lang.Class - El java.lang.Class que es el tipo de datos del objeto.
### getName(int ordinal) {#getName-int}
```
public String getName(int ordinal)
```


Obtiene el valor de la columna especificada como un java.lang.String.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| ordinal | int | El ordinal de columna basado en cero |

**Returns:**
java.lang.String - El nombre de la columna especificada.
### getRecordsAffected() {#getRecordsAffected}
```
public int getRecordsAffected()
```


Obtiene el número de filas insertadas, modificadas o eliminadas por la ejecución de la instrucción SQL.

**Returns:**
int - El [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) no admite esta propiedad y siempre devuelve 0.
### getSchemaTable() {#getSchemaTable}
```
public System.Data.DataTable getSchemaTable()
```


Devuelve un [DataTable](../../com.aspose.words.net.system.data/datatable/) que describe los metadatos de columna del [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that describes the column metadata.
### getValue(int ordinal) {#getValue-int}
```
public Object getValue(int ordinal)
```


Obtiene el valor de la columna especificada en su formato nativo.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| ordinal | int | El ordinal de columna basado en cero |

**Returns:**
java.lang.Object - El valor de la columna especificada. Este método devuelve DBNull para columnas nulas.
### hasRows() {#hasRows}
```
public boolean hasRows()
```


Obtiene un valor que indica si el [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) contiene una o más filas.

**Returns:**
boolean - verdadero si el [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) contiene una o más filas; de lo contrario, falso.
### isClosed() {#isClosed}
```
public boolean isClosed()
```


Obtiene un valor que indica si el [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) está cerrado.

**Returns:**
boolean - Devuelve verdadero si el [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) está cerrado; de lo contrario, falso.
### iterator() {#iterator}
```
public Iterator iterator()
```


Devuelve un enumerador que puede usarse para iterar a través de la colección de elementos.

**Returns:**
java.util.Iterator - Un objeto java.util.Iterator que representa la colección de elementos.
### nextResult() {#nextResult}
```
public boolean nextResult()
```


Avanza el [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) al siguiente conjunto de resultados, si lo hay.

**Returns:**
boolean - verdadero si había otro conjunto de resultados; de lo contrario, falso.
### read() {#read}
```
public boolean read()
```


Avanza el [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) al siguiente registro.

**Returns:**
boolean - verdadero si había otra fila para leer; de lo contrario, falso.
