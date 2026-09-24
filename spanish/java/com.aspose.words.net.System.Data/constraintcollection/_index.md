---
title: "ConstraintCollection"
linktitle: "ConstraintCollection"
second_title: "Aspose.Words para Java"
description: "Representa una colección de restricciones para un DataTable en Java."
type: docs
weight: 11
url: /es/java/com.aspose.words.net.system.data/constraintcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ConstraintCollection implements Iterable
```

Representa una colección de restricciones para un [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Métodos

| Método | Descripción |
| --- | --- |
| [add(System.Data.Constraint constraint)](#add-com.aspose.words.net.System.Data.Constraint) | Agrega el objeto [Constraint](../../com.aspose.words.net.system.data/constraint/) especificado a la colección. |
| [contains(System.Data.Constraint cc)](#contains-com.aspose.words.net.System.Data.Constraint) | Indica si el objeto Constraint especificado por nombre existe en la colección. |
| [get(int index)](#get-int) | Obtiene el [Constraint](../../com.aspose.words.net.system.data/constraint/) de la colección en el índice especificado. |
| [get(String name)](#get-java.lang.String) | Obtiene el [Constraint](../../com.aspose.words.net.system.data/constraint/) de la colección con el nombre especificado. |
| [getCount()](#getCount) | Obtiene el número total de elementos en una colección. |
| [iterator()](#iterator) |  |
| [remove(System.Data.Constraint constraint)](#remove-com.aspose.words.net.System.Data.Constraint) | Elimina el [Constraint](../../com.aspose.words.net.system.data/constraint/) especificado de la colección. |
### add(System.Data.Constraint constraint) {#add-com.aspose.words.net.System.Data.Constraint}
```
public void add(System.Data.Constraint constraint)
```


Agrega el objeto [Constraint](../../com.aspose.words.net.system.data/constraint/) especificado a la colección.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| constraint | [Constraint](../../com.aspose.words.net.system.data/constraint/) | El Constraint a agregar. |

### contains(System.Data.Constraint cc) {#contains-com.aspose.words.net.System.Data.Constraint}
```
public boolean contains(System.Data.Constraint cc)
```


Indica si el objeto Constraint especificado por nombre existe en la colección.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| cc | [Constraint](../../com.aspose.words.net.system.data/constraint/) | El Constraint a eliminar. |

**Returns:**
boolean - true si la colección contiene la restricción especificada; de lo contrario, false.
### get(int index) {#get-int}
```
public System.Data.Constraint get(int index)
```


Obtiene el [Constraint](../../com.aspose.words.net.system.data/constraint/) de la colección en el índice especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | El índice de la restricción a devolver. |

**Returns:**
[Constraint](../../com.aspose.words.net.system.data/constraint/) - The [Constraint](../../com.aspose.words.net.system.data/constraint/) at the specified index.
### get(String name) {#get-java.lang.String}
```
public System.Data.Constraint get(String name)
```


Obtiene el [Constraint](../../com.aspose.words.net.system.data/constraint/) de la colección con el nombre especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| name | java.lang.String | El [Constraint.getConstraintName()](../../com.aspose.words.net.system.data/constraint/\#getConstraintName) / [Constraint.setConstraintName(java.lang.String)](../../com.aspose.words.net.system.data/constraint/\#setConstraintName-java.lang.String) de la restricción a devolver. |

**Returns:**
[Constraint](../../com.aspose.words.net.system.data/constraint/) - The [Constraint](../../com.aspose.words.net.system.data/constraint/) with the specified name; otherwise a null value if the [Constraint](../../com.aspose.words.net.system.data/constraint/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el número total de elementos en una colección.

**Returns:**
int - El número total de elementos en una colección.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(System.Data.Constraint constraint) {#remove-com.aspose.words.net.System.Data.Constraint}
```
public void remove(System.Data.Constraint constraint)
```


Elimina el [Constraint](../../com.aspose.words.net.system.data/constraint/) especificado de la colección.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| constraint | [Constraint](../../com.aspose.words.net.system.data/constraint/) | El [Constraint](../../com.aspose.words.net.system.data/constraint/) a eliminar. |

