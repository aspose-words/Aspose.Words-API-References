---
title: "ConstraintCollection"
linktitle: "ConstraintCollection"
second_title: "Aspose.Words per Java"
description: "Rappresenta una collezione di vincoli per un DataTable in Java."
type: docs
weight: 11
url: /it/java/com.aspose.words.net.system.data/constraintcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ConstraintCollection implements Iterable
```

Rappresenta una collezione di vincoli per un [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [add(System.Data.Constraint constraint)](#add-com.aspose.words.net.System.Data.Constraint) | Aggiunge l'oggetto [Constraint](../../com.aspose.words.net.system.data/constraint/) specificato alla collezione. |
| [contains(System.Data.Constraint cc)](#contains-com.aspose.words.net.System.Data.Constraint) | Indica se l'oggetto Constraint specificato per nome esiste nella collezione. |
| [get(int index)](#get-int) | Ottiene il [Constraint](../../com.aspose.words.net.system.data/constraint/) dalla collezione all'indice specificato. |
| [get(String name)](#get-java.lang.String) | Ottiene il [Constraint](../../com.aspose.words.net.system.data/constraint/) dalla collezione con il nome specificato. |
| [getCount()](#getCount) | Restituisce il numero totale di elementi in una collezione. |
| [iterator()](#iterator) |  |
| [remove(System.Data.Constraint constraint)](#remove-com.aspose.words.net.System.Data.Constraint) | Rimuove il [Constraint](../../com.aspose.words.net.system.data/constraint/) specificato dalla collezione. |
### add(System.Data.Constraint constraint) {#add-com.aspose.words.net.System.Data.Constraint}
```
public void add(System.Data.Constraint constraint)
```


Aggiunge l'oggetto [Constraint](../../com.aspose.words.net.system.data/constraint/) specificato alla collezione.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| constraint | [Constraint](../../com.aspose.words.net.system.data/constraint/) | Il Constraint da aggiungere. |

### contains(System.Data.Constraint cc) {#contains-com.aspose.words.net.System.Data.Constraint}
```
public boolean contains(System.Data.Constraint cc)
```


Indica se l'oggetto Constraint specificato per nome esiste nella collezione.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| cc | [Constraint](../../com.aspose.words.net.system.data/constraint/) | Il Constraint da rimuovere. |

**Returns:**
boolean - true se la collezione contiene il vincolo specificato; altrimenti, false.
### get(int index) {#get-int}
```
public System.Data.Constraint get(int index)
```


Ottiene il [Constraint](../../com.aspose.words.net.system.data/constraint/) dalla collezione all'indice specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice del vincolo da restituire. |

**Returns:**
[Constraint](../../com.aspose.words.net.system.data/constraint/) - The [Constraint](../../com.aspose.words.net.system.data/constraint/) at the specified index.
### get(String name) {#get-java.lang.String}
```
public System.Data.Constraint get(String name)
```


Ottiene il [Constraint](../../com.aspose.words.net.system.data/constraint/) dalla collezione con il nome specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il [Constraint.getConstraintName()](../../com.aspose.words.net.system.data/constraint/\#getConstraintName) / [Constraint.setConstraintName(java.lang.String)](../../com.aspose.words.net.system.data/constraint/\#setConstraintName-java.lang.String) del vincolo da restituire. |

**Returns:**
[Constraint](../../com.aspose.words.net.system.data/constraint/) - The [Constraint](../../com.aspose.words.net.system.data/constraint/) with the specified name; otherwise a null value if the [Constraint](../../com.aspose.words.net.system.data/constraint/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```


Restituisce il numero totale di elementi in una collezione.

**Returns:**
int - Il numero totale di elementi in una collezione.
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


Rimuove il [Constraint](../../com.aspose.words.net.system.data/constraint/) specificato dalla collezione.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| constraint | [Constraint](../../com.aspose.words.net.system.data/constraint/) | Il [Constraint](../../com.aspose.words.net.system.data/constraint/) da rimuovere. |

