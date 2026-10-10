---
title: "KnownTypeSet"
linktitle: "KnownTypeSet"
second_title: "Aspose.Words para Java"
description: "Representa un conjunto no ordenado, es decir, en Java."
type: docs
weight: 412
url: /es/java/com.aspose.words/knowntypeset/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class KnownTypeSet implements Iterable
```

Representa un conjunto no ordenado (es decir, una colección de elementos únicos) que contiene objetos java.lang.Class cuyos nombres totalmente o parcialmente calificados pueden usarse dentro de plantillas de informes para invocar los miembros estáticos de los tipos correspondientes, realizar conversiones de tipo, etc.

Para obtener más información, visite el artículo de documentación [ LINQ Reporting Engine ][LINQ Reporting Engine].


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Métodos

| Método | Descripción |
| --- | --- |
| [add(Class type)](#add-java.lang.Class) | Agrega el objeto java.lang.Class especificado al conjunto. |
| [clear()](#clear) | Elimina todos los elementos del conjunto. |
| [getCount()](#getCount) | Obtiene el recuento de elementos en el conjunto. |
| [iterator()](#iterator) | Devuelve un objeto java.util.Iterator para iterar sobre los elementos del conjunto. |
| [remove(Class type)](#remove-java.lang.Class) | Elimina el objeto java.lang.Class especificado del conjunto. |
### add(Class type) {#add-java.lang.Class}
```
public void add(Class type)
```


Agrega el objeto java.lang.Class especificado al conjunto.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tipo | java.lang.Class | Un objeto java.lang.Class para agregar. |

### clear() {#clear}
```
public void clear()
```


Elimina todos los elementos del conjunto.

### getCount() {#getCount}
```
public int getCount()
```


Obtiene el recuento de elementos en el conjunto.

**Returns:**
int - El recuento de elementos en el conjunto.
### iterator() {#iterator}
```
public Iterator iterator()
```


Devuelve un objeto java.util.Iterator para iterar sobre los elementos del conjunto.

**Returns:**
java.util.Iterator - Un objeto java.util.Iterator para iterar sobre los elementos del conjunto.
### remove(Class type) {#remove-java.lang.Class}
```
public void remove(Class type)
```


Elimina el objeto java.lang.Class especificado del conjunto.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tipo | java.lang.Class | Un objeto java.lang.Class para eliminar. |

