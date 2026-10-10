---
title: "ConstraintCollection"
linktitle: "ConstraintCollection"
second_title: "Aspose.Words für Java"
description: "Stellt eine Sammlung von Einschränkungen für eine DataTable in Java dar."
type: docs
weight: 11
url: /de/java/com.aspose.words.net.system.data/constraintcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ConstraintCollection implements Iterable
```

Stellt eine Sammlung von Einschränkungen für eine [DataTable](../../com.aspose.words.net.system.data/datatable/) dar.
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [add(System.Data.Constraint constraint)](#add-com.aspose.words.net.System.Data.Constraint) | Fügt das angegebene [Constraint](../../com.aspose.words.net.system.data/constraint/) Objekt zur Sammlung hinzu. |
| [contains(System.Data.Constraint cc)](#contains-com.aspose.words.net.System.Data.Constraint) | Gibt an, ob das durch den Namen angegebene Constraint-Objekt in der Sammlung existiert. |
| [get(int index)](#get-int) | Ruft das [Constraint](../../com.aspose.words.net.system.data/constraint/) aus der Sammlung am angegebenen Index ab. |
| [get(String name)](#get-java.lang.String) | Ruft das [Constraint](../../com.aspose.words.net.system.data/constraint/) aus der Sammlung mit dem angegebenen Namen ab. |
| [getCount()](#getCount) | Ermittelt die Gesamtzahl der Elemente in einer Sammlung. |
| [iterator()](#iterator) |  |
| [remove(System.Data.Constraint constraint)](#remove-com.aspose.words.net.System.Data.Constraint) | Entfernt das angegebene [Constraint](../../com.aspose.words.net.system.data/constraint/) aus der Sammlung. |
### add(System.Data.Constraint constraint) {#add-com.aspose.words.net.System.Data.Constraint}
```
public void add(System.Data.Constraint constraint)
```


Fügt das angegebene [Constraint](../../com.aspose.words.net.system.data/constraint/) Objekt zur Sammlung hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| constraint | [Constraint](../../com.aspose.words.net.system.data/constraint/) | Das hinzuzufügende Constraint. |

### contains(System.Data.Constraint cc) {#contains-com.aspose.words.net.System.Data.Constraint}
```
public boolean contains(System.Data.Constraint cc)
```


Gibt an, ob das durch den Namen angegebene Constraint-Objekt in der Sammlung existiert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| cc | [Constraint](../../com.aspose.words.net.system.data/constraint/) | Das zu entfernende Constraint. |

**Returns:**
boolean - true, wenn die Sammlung die angegebene Einschränkung enthält; andernfalls false.
### get(int index) {#get-int}
```
public System.Data.Constraint get(int index)
```


Ruft das [Constraint](../../com.aspose.words.net.system.data/constraint/) aus der Sammlung am angegebenen Index ab.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Der Index des zurückzugebenden Constraints. |

**Returns:**
[Constraint](../../com.aspose.words.net.system.data/constraint/) - The [Constraint](../../com.aspose.words.net.system.data/constraint/) at the specified index.
### get(String name) {#get-java.lang.String}
```
public System.Data.Constraint get(String name)
```


Ruft das [Constraint](../../com.aspose.words.net.system.data/constraint/) aus der Sammlung mit dem angegebenen Namen ab.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der [Constraint.getConstraintName()](../../com.aspose.words.net.system.data/constraint/\#getConstraintName) / [Constraint.setConstraintName(java.lang.String)](../../com.aspose.words.net.system.data/constraint/\#setConstraintName-java.lang.String) des zurückzugebenden Constraints. |

**Returns:**
[Constraint](../../com.aspose.words.net.system.data/constraint/) - The [Constraint](../../com.aspose.words.net.system.data/constraint/) with the specified name; otherwise a null value if the [Constraint](../../com.aspose.words.net.system.data/constraint/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```


Ermittelt die Gesamtzahl der Elemente in einer Sammlung.

**Returns:**
int - Die Gesamtzahl der Elemente in einer Sammlung.
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


Entfernt das angegebene [Constraint](../../com.aspose.words.net.system.data/constraint/) aus der Sammlung.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| constraint | [Constraint](../../com.aspose.words.net.system.data/constraint/) | Das zu entfernende [Constraint](../../com.aspose.words.net.system.data/constraint/). |

