---
title: "DataRelationCollection"
linktitle: "DataRelationCollection"
second_title: "Aspose.Words para Java"
description: "Representa la colección de objetos DataRelation para este DataSet en Java."
type: docs
weight: 19
url: /es/java/com.aspose.words.net.system.data/datarelationcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataRelationCollection implements Iterable
```

Representa la colección de objetos [DataRelation](../../com.aspose.words.net.system.data/datarelation/) para este [DataSet](../../com.aspose.words.net.system.data/dataset/).
## Métodos

| Método | Descripción |
| --- | --- |
| [add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#add-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Crea un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) con una columna padre y una columna hija especificadas, y lo agrega a la colección. |
| [add(System.Data.DataRelation relation)](#add-com.aspose.words.net.System.Data.DataRelation) | Agrega un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) a la [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| [add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName)](#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String-java.lang.String) | Agrega una relación a la colección. |
| [add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)](#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String) | Agrega una relación a la colección. |
| [add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Crea un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) con el nombre especificado, y columnas padre e hija, y lo agrega a la colección. |
| [add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)](#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean) | Crea un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) con el nombre especificado, columnas padre e hija, con restricciones opcionales según el valor del parámetro  createConstraints , y lo agrega a la colección. |
| [clear()](#clear) | Limpia la colección de cualquier relación. |
| [contains(System.Data.DataRelation relation)](#contains-com.aspose.words.net.System.Data.DataRelation) | Verifica si existe un DataRelation con el nombre específico (sin distinción de mayúsculas) en la colección. |
| [get(int index)](#get-int) | Obtiene el objeto [DataRelation](../../com.aspose.words.net.system.data/datarelation/) en el índice especificado. |
| [get(String name)](#get-java.lang.String) | Obtiene el objeto [DataRelation](../../com.aspose.words.net.system.data/datarelation/) especificado por nombre. |
| [getCount()](#getCount) |  |
| [indexOf(System.Data.DataRelation relation)](#indexOf-com.aspose.words.net.System.Data.DataRelation) | Obtiene el índice del objeto [DataRelation](../../com.aspose.words.net.system.data/datarelation/) especificado. |
| [iterator()](#iterator) |  |
| [removeAt(int index)](#removeAt-int) | Elimina la relación en el índice especificado de la colección. |
### add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#add-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public void add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Crea un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) con una columna padre y una columna hija especificadas, y lo agrega a la colección.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La columna padre de la relación. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La columna hija de la relación. |

### add(System.Data.DataRelation relation) {#add-com.aspose.words.net.System.Data.DataRelation}
```
public void add(System.Data.DataRelation relation)
```


Agrega un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) a la [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | El DataRelation a agregar a la colección. |

### add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName) {#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String-java.lang.String}
```
public void add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName)
```


Agrega una relación a la colección. No realiza verificaciones de duplicados, etc.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | La tabla padre de la relación. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | La tabla hija de la relación. |
| parentColumnName | java.lang.String | El nombre de la columna padre de la relación. |
| childColumnName | java.lang.String | El nombre de la columna hija de la relación. |

### add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames) {#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String}
```
public void add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)
```


Agrega una relación a la colección. No realiza verificaciones de duplicados, etc.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | La tabla padre de la relación. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | La tabla hija de la relación. |
| parentColumnNames | java.lang.String[] | El arreglo del nombre de la columna padre de la relación. |
| childColumnNames | java.lang.String[] | El arreglo del nombre de la columna hija de la relación. |

### add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public void add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Crea un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) con el nombre especificado, y columnas padre e hija, y lo agrega a la colección.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre de la relación. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La columna padre de la relación. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La columna hija de la relación. |

### add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints) {#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean}
```
public void add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)
```


Crea un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) con el nombre especificado, columnas padre e hija, con restricciones opcionales según el valor del parámetro  createConstraints , y lo agrega a la colección.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre de la relación. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La columna padre de la relación. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La columna hija de la relación. |
| createConstraints | boolean | true para crear restricciones; de lo contrario false. (El valor predeterminado es true). |

### clear() {#clear}
```
public void clear()
```


Limpia la colección de cualquier relación.

### contains(System.Data.DataRelation relation) {#contains-com.aspose.words.net.System.Data.DataRelation}
```
public boolean contains(System.Data.DataRelation relation)
```


Verifica si existe un DataRelation con el nombre específico (sin distinción de mayúsculas) en la colección.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | El nombre de la relación a buscar. |

**Returns:**
boolean - true, si existe una relación con el nombre especificado; de lo contrario false.
### get(int index) {#get-int}
```
public System.Data.DataRelation get(int index)
```


Obtiene el objeto [DataRelation](../../com.aspose.words.net.system.data/datarelation/) en el índice especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | El índice basado en cero a buscar. |

**Returns:**
[DataRelation](../../com.aspose.words.net.system.data/datarelation/) - The [DataRelation](../../com.aspose.words.net.system.data/datarelation/), or a null value if the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/) does not exist.
### get(String name) {#get-java.lang.String}
```
public System.Data.DataRelation get(String name)
```


Obtiene el objeto [DataRelation](../../com.aspose.words.net.system.data/datarelation/) especificado por nombre.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre de la relación a buscar. |

**Returns:**
[DataRelation](../../com.aspose.words.net.system.data/datarelation/) - The named [DataRelation](../../com.aspose.words.net.system.data/datarelation/), or a null value if the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int - el número total de elementos en una colección
### indexOf(System.Data.DataRelation relation) {#indexOf-com.aspose.words.net.System.Data.DataRelation}
```
public int indexOf(System.Data.DataRelation relation)
```


Obtiene el índice del objeto [DataRelation](../../com.aspose.words.net.system.data/datarelation/) especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | La relación a buscar. |

**Returns:**
int - El índice basado en cero de la relación, o -1 si la relación no se encuentra en la colección.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Elimina la relación en el índice especificado de la colección.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | El índice de la relación a eliminar. |

