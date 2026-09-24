---
title: "DataColumnCollection"
linktitle: "DataColumnCollection"
second_title: "Aspose.Words para Java"
description: "Representa una colección de objetos DataColumn para un DataTable en Java."
type: docs
weight: 15
url: /es/java/com.aspose.words.net.system.data/datacolumncollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataColumnCollection implements Iterable
```

Representa una colección de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) para un [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Métodos

| Método | Descripción |
| --- | --- |
| [add(System.Data.DataColumn column)](#add-com.aspose.words.net.System.Data.DataColumn) | Crea y agrega el objeto [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) especificado a la [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [add(String columnName)](#add-java.lang.String) | Crea y agrega un objeto [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) que tiene el nombre especificado a la [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [add(String columnName, Class type)](#add-java.lang.String-java.lang.Class) | Crea y agrega un objeto [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) que tiene el nombre y tipo especificados a la [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull)](#add-java.lang.String-java.lang.Class-int-boolean-boolean) | Crea y agrega un [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) con el nombre, tipo y valores específicos especificados a la colección de columnas. |
| [clear()](#clear) | Limpia la colección de cualquier columna. |
| [contains(String name)](#contains-java.lang.String) | Comprueba si la colección contiene una columna con el nombre especificado. |
| [get(int index)](#get-int) | Obtiene el [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) de la colección en el índice especificado. |
| [get(String name)](#get-java.lang.String) | Obtiene el [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) de la colección con el nombre especificado. |
| [getCount()](#getCount) |  |
| [indexOf(System.Data.DataColumn column)](#indexOf-com.aspose.words.net.System.Data.DataColumn) | Obtiene el índice de una columna especificada por nombre. |
| [indexOf(String columnName)](#indexOf-java.lang.String) | Obtiene el índice de la columna con el nombre específico (el nombre no distingue entre mayúsculas y minúsculas). |
| [iterator()](#iterator) |  |
| [remove(System.Data.DataColumn column)](#remove-com.aspose.words.net.System.Data.DataColumn) | Elimina el objeto [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) especificado de la colección. |
| [remove(String name)](#remove-java.lang.String) | Elimina el objeto [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) que tiene el nombre especificado de la colección. |
### add(System.Data.DataColumn column) {#add-com.aspose.words.net.System.Data.DataColumn}
```
public void add(System.Data.DataColumn column)
```


Crea y agrega el objeto [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) especificado a la [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | El [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) a agregar. |

### add(String columnName) {#add-java.lang.String}
```
public void add(String columnName)
```


Crea y agrega un objeto [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) que tiene el nombre especificado a la [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| columnName | java.lang.String | El nombre de la columna. |

### add(String columnName, Class type) {#add-java.lang.String-java.lang.Class}
```
public System.Data.DataColumn add(String columnName, Class type)
```


Crea y agrega un objeto [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) que tiene el nombre y tipo especificados a la [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| columnName | java.lang.String | El [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) a usar cuando crea la columna. |
| type | java.lang.Class | El [DataColumn.getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [DataColumn.setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class) de la nueva columna. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The newly created [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull) {#add-java.lang.String-java.lang.Class-int-boolean-boolean}
```
public System.Data.DataColumn add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull)
```


Crea y agrega un [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) con el nombre, tipo y valores específicos especificados a la colección de columnas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| columnName | java.lang.String | nombre |
| tipo | java.lang.Class | tipo de datos |
| columnMapping | int | tipo de mapeo de columna |
| allowAutoIncrement | boolean | se permite el auto incremento |
| allowDBNull | boolean | se permite el valor DBNull |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - created a [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) instance.
### clear() {#clear}
```
public void clear()
```


Limpia la colección de cualquier columna.

### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Comprueba si la colección contiene una columna con el nombre especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| name | java.lang.String | El [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) de la columna a buscar. |

**Returns:**
booleano - verdadero si existe una columna con este nombre; de lo contrario, falso.
### get(int index) {#get-int}
```
public System.Data.DataColumn get(int index)
```


Obtiene el [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) de la colección en el índice especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | El índice basado en cero de la columna a devolver. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) at the specified index.
### get(String name) {#get-java.lang.String}
```
public System.Data.DataColumn get(String name)
```


Obtiene el [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) de la colección con el nombre especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| name | java.lang.String | El [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) de la columna a devolver. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in the collection with the specified [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String); otherwise a null value if the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int - el número total de elementos en una colección.
### indexOf(System.Data.DataColumn column) {#indexOf-com.aspose.words.net.System.Data.DataColumn}
```
public int indexOf(System.Data.DataColumn column)
```


Obtiene el índice de una columna especificada por nombre.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | El nombre de la columna a devolver. |

**Returns:**
int - El índice de la columna especificada por  column  si se encuentra; de lo contrario, -1.
### indexOf(String columnName) {#indexOf-java.lang.String}
```
public int indexOf(String columnName)
```


Obtiene el índice de la columna con el nombre específico (el nombre no distingue entre mayúsculas y minúsculas).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| columnName | java.lang.String | El nombre de la columna a buscar. |

**Returns:**
int - El índice basado en cero de la columna con el nombre especificado, o -1 si la columna no existe en la colección.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(System.Data.DataColumn column) {#remove-com.aspose.words.net.System.Data.DataColumn}
```
public void remove(System.Data.DataColumn column)
```


Elimina el objeto [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) especificado de la colección.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | El [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) a eliminar. |

### remove(String name) {#remove-java.lang.String}
```
public void remove(String name)
```


Elimina el objeto [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) que tiene el nombre especificado de la colección.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre de la columna a eliminar. |

