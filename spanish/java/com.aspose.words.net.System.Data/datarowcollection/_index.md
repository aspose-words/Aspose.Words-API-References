---
title: "DataRowCollection"
linktitle: "DataRowCollection"
second_title: "Aspose.Words para Java"
description: "Representa una colección de filas para un DataTable en Java."
type: docs
weight: 21
url: /es/java/com.aspose.words.net.system.data/datarowcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataRowCollection implements Iterable
```

Representa una colección de filas para un [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Métodos

| Método | Descripción |
| --- | --- |
| [add(System.Data.DataRow row)](#add-com.aspose.words.net.System.Data.DataRow) | Agrega el [DataRow](../../com.aspose.words.net.system.data/datarow/) especificado al objeto [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/). |
| [add(Object[] values)](#add-java.lang.Object...) | Crea una fila usando los valores especificados y la agrega al [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/). |
| [clear()](#clear) | Limpia la colección de todas las filas. |
| [find(Object[] keys)](#find-java.lang.Object) | Obtiene la fila que contiene los valores de clave primaria especificados. |
| [find(String primaryKeyValue)](#find-java.lang.String) | Obtiene la fila especificada por el valor de la clave primaria. |
| [get(int index)](#get-int) | Obtiene la fila en el índice especificado. |
| [get(Object[] values)](#get-java.lang.Object) | Obtiene la fila que contiene los valores especificados. |
| [getCount()](#getCount) | Obtiene el número total de objetos [DataRow](../../com.aspose.words.net.system.data/datarow/) en esta colección. |
| [insertAt(System.Data.DataRow row, int pos)](#insertAt-com.aspose.words.net.System.Data.DataRow-int) | Inserta una nueva fila en la colección en la ubicación especificada. |
| [iterator()](#iterator) | Obtiene un java.util.Iterator para esta colección. |
| [removeAt(int index)](#removeAt-int) | Elimina la fila en el índice especificado de la colección. |
### add(System.Data.DataRow row) {#add-com.aspose.words.net.System.Data.DataRow}
```
public void add(System.Data.DataRow row)
```


Agrega el [DataRow](../../com.aspose.words.net.system.data/datarow/) especificado al objeto [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) | El [DataRow](../../com.aspose.words.net.system.data/datarow/) a agregar. |

### add(Object[] values) {#add-java.lang.Object...}
```
public void add(Object[] values)
```


Crea una fila usando los valores especificados y la agrega al [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valores | java.lang.Object[] | La matriz de valores que se utilizan para crear la nueva fila. |

### clear() {#clear}
```
public void clear()
```


Limpia la colección de todas las filas.

### find(Object[] keys) {#find-java.lang.Object}
```
public System.Data.DataRow find(Object[] keys)
```


Obtiene la fila que contiene los valores de clave primaria especificados.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| claves | java.lang.Object[] | Una matriz de valores de clave primaria para buscar. El tipo de la matriz es Object. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A [DataRow](../../com.aspose.words.net.system.data/datarow/) object that contains the primary key values specified; otherwise a null value if the primary key value does not exist in the [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).
### find(String primaryKeyValue) {#find-java.lang.String}
```
public System.Data.DataRow find(String primaryKeyValue)
```


Obtiene la fila especificada por el valor de la clave primaria.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| primaryKeyValue | java.lang.String | El valor de la clave primaria del DataRow a buscar. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A DataRow that contains the primary key value specified; otherwise a null value if the primary key value does not exist in the DataRowCollection.
### get(int index) {#get-int}
```
public System.Data.DataRow get(int index)
```


Obtiene la fila en el índice especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | El índice basado en cero de la fila a devolver. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - The specified [DataRow](../../com.aspose.words.net.system.data/datarow/).
### get(Object[] values) {#get-java.lang.Object}
```
public System.Data.DataRow get(Object[] values)
```


Obtiene la fila que contiene los valores especificados. Si hay columnas de clave primaria presentes, se usará el índice. Si no hay índice, se utilizará un escaneo lineal simple. Tenga cuidado con eso porque podría tomar una cantidad significativa de tiempo.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valores | java.lang.Object[] | datos de la fila |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - found row or `null`
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el número total de objetos [DataRow](../../com.aspose.words.net.system.data/datarow/) en esta colección.

**Returns:**
int - El número total de objetos [DataRow](../../com.aspose.words.net.system.data/datarow/) en esta colección.
### insertAt(System.Data.DataRow row, int pos) {#insertAt-com.aspose.words.net.System.Data.DataRow-int}
```
public void insertAt(System.Data.DataRow row, int pos)
```


Inserta una nueva fila en la colección en la ubicación especificada.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) | El [DataRow](../../com.aspose.words.net.system.data/datarow/) a agregar. |
| pos | int | La ubicación (basada en cero) en la colección donde desea agregar el DataRow. |

### iterator() {#iterator}
```
public Iterator iterator()
```


Obtiene un java.util.Iterator para esta colección.

**Returns:**
java.util.Iterator - Un java.util.Iterator para esta colección.
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Elimina la fila en el índice especificado de la colección.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | El índice de la fila a eliminar. |

