---
title: "ConstraintCollection"
linktitle: "ConstraintCollection"
second_title: "Aspose.Words pour Java"
description: "Représente une collection de contraintes pour un DataTable en Java."
type: docs
weight: 11
url: /fr/java/com.aspose.words.net.system.data/constraintcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ConstraintCollection implements Iterable
```

Représente une collection de contraintes pour un [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Méthodes

| Méthode | Description |
| --- | --- |
| [add(System.Data.Constraint constraint)](#add-com.aspose.words.net.System.Data.Constraint) | Ajoute l'objet [Constraint](../../com.aspose.words.net.system.data/constraint/) spécifié à la collection. |
| [contains(System.Data.Constraint cc)](#contains-com.aspose.words.net.System.Data.Constraint) | Indique si l'objet Constraint spécifié par son nom existe dans la collection. |
| [get(int index)](#get-int) | Obtient le [Constraint](../../com.aspose.words.net.system.data/constraint/) de la collection à l'index spécifié. |
| [get(String name)](#get-java.lang.String) | Obtient le [Constraint](../../com.aspose.words.net.system.data/constraint/) de la collection avec le nom spécifié. |
| [getCount()](#getCount) | Obtient le nombre total d'éléments dans une collection. |
| [iterator()](#iterator) |  |
| [remove(System.Data.Constraint constraint)](#remove-com.aspose.words.net.System.Data.Constraint) | Supprime le [Constraint](../../com.aspose.words.net.system.data/constraint/) spécifié de la collection. |
### add(System.Data.Constraint constraint) {#add-com.aspose.words.net.System.Data.Constraint}
```
public void add(System.Data.Constraint constraint)
```


Ajoute l'objet [Constraint](../../com.aspose.words.net.system.data/constraint/) spécifié à la collection.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| constraint | [Constraint](../../com.aspose.words.net.system.data/constraint/) | Le Constraint à ajouter. |

### contains(System.Data.Constraint cc) {#contains-com.aspose.words.net.System.Data.Constraint}
```
public boolean contains(System.Data.Constraint cc)
```


Indique si l'objet Constraint spécifié par son nom existe dans la collection.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| cc | [Constraint](../../com.aspose.words.net.system.data/constraint/) | Le Constraint à supprimer. |

**Returns:**
boolean - true si la collection contient la contrainte spécifiée ; sinon, false.
### get(int index) {#get-int}
```
public System.Data.Constraint get(int index)
```


Obtient le [Constraint](../../com.aspose.words.net.system.data/constraint/) de la collection à l'index spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | L'index de la contrainte à retourner. |

**Returns:**
[Constraint](../../com.aspose.words.net.system.data/constraint/) - The [Constraint](../../com.aspose.words.net.system.data/constraint/) at the specified index.
### get(String name) {#get-java.lang.String}
```
public System.Data.Constraint get(String name)
```


Obtient le [Constraint](../../com.aspose.words.net.system.data/constraint/) de la collection avec le nom spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| name | java.lang.String | Le [Constraint.getConstraintName()](../../com.aspose.words.net.system.data/constraint/\#getConstraintName) / [Constraint.setConstraintName(java.lang.String)](../../com.aspose.words.net.system.data/constraint/\#setConstraintName-java.lang.String) de la contrainte à retourner. |

**Returns:**
[Constraint](../../com.aspose.words.net.system.data/constraint/) - The [Constraint](../../com.aspose.words.net.system.data/constraint/) with the specified name; otherwise a null value if the [Constraint](../../com.aspose.words.net.system.data/constraint/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```


Obtient le nombre total d'éléments dans une collection.

**Returns:**
int - Le nombre total d'éléments dans une collection.
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


Supprime le [Constraint](../../com.aspose.words.net.system.data/constraint/) spécifié de la collection.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| constraint | [Constraint](../../com.aspose.words.net.system.data/constraint/) | Le [Constraint](../../com.aspose.words.net.system.data/constraint/) à supprimer. |

