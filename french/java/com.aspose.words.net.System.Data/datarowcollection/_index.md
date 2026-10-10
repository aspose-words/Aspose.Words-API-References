---
title: "DataRowCollection"
linktitle: "DataRowCollection"
second_title: "Aspose.Words pour Java"
description: "Représente une collection de lignes pour un DataTable en Java."
type: docs
weight: 21
url: /fr/java/com.aspose.words.net.system.data/datarowcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataRowCollection implements Iterable
```

Représente une collection de lignes pour le [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Méthodes

| Méthode | Description |
| --- | --- |
| [add(System.Data.DataRow row)](#add-com.aspose.words.net.System.Data.DataRow) | Ajoute le [DataRow](../../com.aspose.words.net.system.data/datarow/) spécifié à l'objet [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/). |
| [add(Object[] values)](#add-java.lang.Object...) | Crée une ligne en utilisant les valeurs spécifiées et l'ajoute au [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/). |
| [clear()](#clear) | Vide la collection de toutes les lignes. |
| [find(Object[] keys)](#find-java.lang.Object) | Obtient la ligne qui contient les valeurs de clé primaire spécifiées. |
| [find(String primaryKeyValue)](#find-java.lang.String) | Obtient la ligne spécifiée par la valeur de clé primaire. |
| [get(int index)](#get-int) | Obtient la ligne à l'index spécifié. |
| [get(Object[] values)](#get-java.lang.Object) | Obtient la ligne qui contient les valeurs spécifiées. |
| [getCount()](#getCount) | Obtient le nombre total d'objets [DataRow](../../com.aspose.words.net.system.data/datarow/) dans cette collection. |
| [insertAt(System.Data.DataRow row, int pos)](#insertAt-com.aspose.words.net.System.Data.DataRow-int) | Insère une nouvelle ligne dans la collection à l'emplacement spécifié. |
| [iterator()](#iterator) | Obtient un java.util.Iterator pour cette collection. |
| [removeAt(int index)](#removeAt-int) | Supprime la ligne à l'index spécifié de la collection. |
### add(System.Data.DataRow row) {#add-com.aspose.words.net.System.Data.DataRow}
```
public void add(System.Data.DataRow row)
```


Ajoute le [DataRow](../../com.aspose.words.net.system.data/datarow/) spécifié à l'objet [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Le [DataRow](../../com.aspose.words.net.system.data/datarow/) à ajouter. |

### add(Object[] values) {#add-java.lang.Object...}
```
public void add(Object[] values)
```


Crée une ligne en utilisant les valeurs spécifiées et l'ajoute au [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeurs | java.lang.Object[] | Le tableau de valeurs utilisé pour créer la nouvelle ligne. |

### clear() {#clear}
```
public void clear()
```


Vide la collection de toutes les lignes.

### find(Object[] keys) {#find-java.lang.Object}
```
public System.Data.DataRow find(Object[] keys)
```


Obtient la ligne qui contient les valeurs de clé primaire spécifiées.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| clés | java.lang.Object[] | Un tableau de valeurs de clé primaire à rechercher. Le type du tableau est Object. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A [DataRow](../../com.aspose.words.net.system.data/datarow/) object that contains the primary key values specified; otherwise a null value if the primary key value does not exist in the [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).
### find(String primaryKeyValue) {#find-java.lang.String}
```
public System.Data.DataRow find(String primaryKeyValue)
```


Obtient la ligne spécifiée par la valeur de clé primaire.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| primaryKeyValue | java.lang.String | La valeur de la clé primaire du DataRow à rechercher. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A DataRow that contains the primary key value specified; otherwise a null value if the primary key value does not exist in the DataRowCollection.
### get(int index) {#get-int}
```
public System.Data.DataRow get(int index)
```


Obtient la ligne à l'index spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | L'index basé sur zéro de la ligne à renvoyer. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - The specified [DataRow](../../com.aspose.words.net.system.data/datarow/).
### get(Object[] values) {#get-java.lang.Object}
```
public System.Data.DataRow get(Object[] values)
```


Obtient la ligne qui contient les valeurs spécifiées. Si les colonnes de clé primaire sont présentes, alors l'index sera utilisé. S'il n'y a pas d'index, alors un simple balayage linéaire est utilisé. Soyez prudent avec cela car cela peut prendre un temps considérable.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeurs | java.lang.Object[] | données de la ligne |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - found row or `null`
### getCount() {#getCount}
```
public int getCount()
```


Obtient le nombre total d'objets [DataRow](../../com.aspose.words.net.system.data/datarow/) dans cette collection.

**Returns:**
int - Le nombre total d'objets [DataRow](../../com.aspose.words.net.system.data/datarow/) dans cette collection.
### insertAt(System.Data.DataRow row, int pos) {#insertAt-com.aspose.words.net.System.Data.DataRow-int}
```
public void insertAt(System.Data.DataRow row, int pos)
```


Insère une nouvelle ligne dans la collection à l'emplacement spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Le [DataRow](../../com.aspose.words.net.system.data/datarow/) à ajouter. |
| pos | int | L'emplacement (basé sur zéro) dans la collection où vous souhaitez ajouter le DataRow. |

### iterator() {#iterator}
```
public Iterator iterator()
```


Obtient un java.util.Iterator pour cette collection.

**Returns:**
java.util.Iterator - Un java.util.Iterator pour cette collection.
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Supprime la ligne à l'index spécifié de la collection.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | L'index de la ligne à supprimer. |

