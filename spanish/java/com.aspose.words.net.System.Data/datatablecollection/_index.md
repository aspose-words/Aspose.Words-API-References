---
title: "DataTableCollection"
linktitle: "DataTableCollection"
second_title: "Aspose.Words para Java"
description: "Representa la colección de tablas para el DataSet en Java."
type: docs
weight: 26
url: /es/java/com.aspose.words.net.system.data/datatablecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataTableCollection implements Iterable
```

Representa la colección de tablas para el [DataSet](../../com.aspose.words.net.system.data/dataset/).
## Métodos

| Método | Descripción |
| --- | --- |
| [add(System.Data.DataTable table)](#add-com.aspose.words.net.System.Data.DataTable) | Agrega la DataTable especificada a la colección. |
| [add(String name)](#add-java.lang.String) | Crea un objeto [DataTable](../../com.aspose.words.net.system.data/datatable/) usando el nombre especificado y lo agrega a la colección. |
| [contains(String name)](#contains-java.lang.String) | Obtiene un valor que indica si un objeto [DataTable](../../com.aspose.words.net.system.data/datatable/) con el nombre especificado existe en la colección. |
| [get(int index)](#get-int) | Obtiene el objeto [DataTable](../../com.aspose.words.net.system.data/datatable/) en el índice especificado. |
| [get(String name)](#get-java.lang.String) | Obtiene el objeto [DataTable](../../com.aspose.words.net.system.data/datatable/) con el nombre especificado. |
| [get(String name, String tableNamespace)](#get-java.lang.String-java.lang.String) | Obtiene el objeto [DataTable](../../com.aspose.words.net.system.data/datatable/) con el nombre especificado en el espacio de nombres especificado. |
| [getCount()](#getCount) |  |
| [iterator()](#iterator) |  |
| [remove(String name)](#remove-java.lang.String) | Elimina el objeto [DataTable](../../com.aspose.words.net.system.data/datatable/) con el nombre especificado de la colección. |
### add(System.Data.DataTable table) {#add-com.aspose.words.net.System.Data.DataTable}
```
public void add(System.Data.DataTable table)
```


Agrega la DataTable especificada a la colección.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | El objeto DataTable a agregar. |

### add(String name) {#add-java.lang.String}
```
public System.Data.DataTable add(String name)
```


Crea un objeto [DataTable](../../com.aspose.words.net.system.data/datatable/) usando el nombre especificado y lo agrega a la colección.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| name | java.lang.String | El nombre que se le asignará al [DataTable](../../com.aspose.words.net.system.data/datatable/) creado. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The newly created [DataTable](../../com.aspose.words.net.system.data/datatable/).
### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Obtiene un valor que indica si un objeto [DataTable](../../com.aspose.words.net.system.data/datatable/) con el nombre especificado existe en la colección.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| name | java.lang.String | El nombre del [DataTable](../../com.aspose.words.net.system.data/datatable/) a buscar. |

**Returns:**
boolean - true si la tabla especificada existe; de lo contrario false.
### get(int index) {#get-int}
```
public System.Data.DataTable get(int index)
```


Obtiene el objeto [DataTable](../../com.aspose.words.net.system.data/datatable/) en el índice especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| index | int | El índice basado en cero del [DataTable](../../com.aspose.words.net.system.data/datatable/) a buscar. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/).
### get(String name) {#get-java.lang.String}
```
public System.Data.DataTable get(String name)
```


Obtiene el objeto [DataTable](../../com.aspose.words.net.system.data/datatable/) con el nombre especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre del DataTable a buscar. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) with the specified name; otherwise null if the [DataTable](../../com.aspose.words.net.system.data/datatable/) does not exist.
### get(String name, String tableNamespace) {#get-java.lang.String-java.lang.String}
```
public System.Data.DataTable get(String name, String tableNamespace)
```


Obtiene el objeto [DataTable](../../com.aspose.words.net.system.data/datatable/) con el nombre especificado en el espacio de nombres especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre del DataTable a buscar. |
| tableNamespace | java.lang.String | El nombre del espacio de nombres [DataTable](../../com.aspose.words.net.system.data/datatable/) en el que buscar. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) with the specified name; otherwise null if the [DataTable](../../com.aspose.words.net.system.data/datatable/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int - número total de elementos en esta colección.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(String name) {#remove-java.lang.String}
```
public System.Data.DataTable remove(String name)
```


Elimina el objeto [DataTable](../../com.aspose.words.net.system.data/datatable/) con el nombre especificado de la colección.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| name | java.lang.String | El nombre del objeto [DataTable](../../com.aspose.words.net.system.data/datatable/) a eliminar. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/)
