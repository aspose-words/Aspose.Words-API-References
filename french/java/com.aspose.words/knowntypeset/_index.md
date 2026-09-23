---
title: "KnownTypeSet"
linktitle: "KnownTypeSet"
second_title: "Aspose.Words pour Java"
description: "Représente un ensemble non ordonné, c.-à-d. en Java."
type: docs
weight: 412
url: /fr/java/com.aspose.words/knowntypeset/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class KnownTypeSet implements Iterable
```

Représente un ensemble non ordonné (c.-à-d. une collection d'éléments uniques) contenant des objets java.lang.Class dont les noms entièrement ou partiellement qualifiés peuvent être utilisés dans les modèles de rapport pour invoquer les membres statiques des types correspondants, effectuer des conversions de type, etc.

Pour en savoir plus, consultez l'article de documentation [ LINQ Reporting Engine ][LINQ Reporting Engine].


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Méthodes

| Méthode | Description |
| --- | --- |
| [add(Class type)](#add-java.lang.Class) | Ajoute l'objet java.lang.Class spécifié à l'ensemble. |
| [clear()](#clear) | Supprime tous les éléments de l'ensemble. |
| [getCount()](#getCount) | Obtient le nombre d'éléments dans l'ensemble. |
| [iterator()](#iterator) | Renvoie un objet java.util.Iterator pour parcourir les éléments de l'ensemble. |
| [remove(Class type)](#remove-java.lang.Class) | Supprime l'objet java.lang.Class spécifié de l'ensemble. |
### add(Class type) {#add-java.lang.Class}
```
public void add(Class type)
```


Ajoute l'objet java.lang.Class spécifié à l'ensemble.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| type | java.lang.Class | Un objet java.lang.Class à ajouter. |

### clear() {#clear}
```
public void clear()
```


Supprime tous les éléments de l'ensemble.

### getCount() {#getCount}
```
public int getCount()
```


Obtient le nombre d'éléments dans l'ensemble.

**Returns:**
int - Le nombre d'éléments dans l'ensemble.
### iterator() {#iterator}
```
public Iterator iterator()
```


Renvoie un objet java.util.Iterator pour parcourir les éléments de l'ensemble.

**Returns:**
java.util.Iterator - Un objet java.util.Iterator pour parcourir les éléments de l'ensemble.
### remove(Class type) {#remove-java.lang.Class}
```
public void remove(Class type)
```


Supprime l'objet java.lang.Class spécifié de l'ensemble.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| type | java.lang.Class | Un objet java.lang.Class à supprimer. |

