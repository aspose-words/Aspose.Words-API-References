---
title: "DataTableCollection"
linktitle: "DataTableCollection"
second_title: "Aspose.Words pour Java"
description: "Représente la collection de tables du DataSet en Java."
type: docs
weight: 26
url: /fr/java/com.aspose.words.net.system.data/datatablecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataTableCollection implements Iterable
```

Représente la collection de tables du [DataSet](../../com.aspose.words.net.system.data/dataset/).
## Méthodes

| Méthode | Description |
| --- | --- |
| [add(System.Data.DataTable table)](#add-com.aspose.words.net.System.Data.DataTable) | Ajoute le DataTable spécifié à la collection. |
| [add(String name)](#add-java.lang.String) | Crée un objet [DataTable](../../com.aspose.words.net.system.data/datatable/) en utilisant le nom spécifié et l'ajoute à la collection. |
| [contains(String name)](#contains-java.lang.String) | Obtient une valeur indiquant si un objet [DataTable](../../com.aspose.words.net.system.data/datatable/) avec le nom spécifié existe dans la collection. |
| [get(int index)](#get-int) | Obtient l'objet [DataTable](../../com.aspose.words.net.system.data/datatable/) à l'index spécifié. |
| [get(String name)](#get-java.lang.String) | Obtient l'objet [DataTable](../../com.aspose.words.net.system.data/datatable/) avec le nom spécifié. |
| [get(String name, String tableNamespace)](#get-java.lang.String-java.lang.String) | Obtient l'objet [DataTable](../../com.aspose.words.net.system.data/datatable/) avec le nom spécifié dans l'espace de noms spécifié. |
| [getCount()](#getCount) |  |
| [iterator()](#iterator) |  |
| [remove(String name)](#remove-java.lang.String) | Supprime l'objet [DataTable](../../com.aspose.words.net.system.data/datatable/) avec le nom spécifié de la collection. |
### add(System.Data.DataTable table) {#add-com.aspose.words.net.System.Data.DataTable}
```
public void add(System.Data.DataTable table)
```


Ajoute le DataTable spécifié à la collection.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | L'objet DataTable à ajouter. |

### add(String name) {#add-java.lang.String}
```
public System.Data.DataTable add(String name)
```


Crée un objet [DataTable](../../com.aspose.words.net.system.data/datatable/) en utilisant le nom spécifié et l'ajoute à la collection.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| name | java.lang.String | Le nom à attribuer au [DataTable](../../com.aspose.words.net.system.data/datatable/) créé. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The newly created [DataTable](../../com.aspose.words.net.system.data/datatable/).
### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Obtient une valeur indiquant si un objet [DataTable](../../com.aspose.words.net.system.data/datatable/) avec le nom spécifié existe dans la collection.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| name | java.lang.String | Le nom du [DataTable](../../com.aspose.words.net.system.data/datatable/) à rechercher. |

**Returns:**
booléen - vrai si la table spécifiée existe ; sinon faux.
### get(int index) {#get-int}
```
public System.Data.DataTable get(int index)
```


Obtient l'objet [DataTable](../../com.aspose.words.net.system.data/datatable/) à l'index spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | L'index de base zéro du [DataTable](../../com.aspose.words.net.system.data/datatable/) à rechercher. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/).
### get(String name) {#get-java.lang.String}
```
public System.Data.DataTable get(String name)
```


Obtient l'objet [DataTable](../../com.aspose.words.net.system.data/datatable/) avec le nom spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom du DataTable à rechercher. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) with the specified name; otherwise null if the [DataTable](../../com.aspose.words.net.system.data/datatable/) does not exist.
### get(String name, String tableNamespace) {#get-java.lang.String-java.lang.String}
```
public System.Data.DataTable get(String name, String tableNamespace)
```


Obtient l'objet [DataTable](../../com.aspose.words.net.system.data/datatable/) avec le nom spécifié dans l'espace de noms spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom du DataTable à rechercher. |
| tableNamespace | java.lang.String | Le nom de l'espace de noms du [DataTable](../../com.aspose.words.net.system.data/datatable/) dans lequel chercher. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) with the specified name; otherwise null if the [DataTable](../../com.aspose.words.net.system.data/datatable/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int - nombre total d'éléments dans cette collection.
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


Supprime l'objet [DataTable](../../com.aspose.words.net.system.data/datatable/) avec le nom spécifié de la collection.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| name | java.lang.String | Le nom de l'objet [DataTable](../../com.aspose.words.net.system.data/datatable/) à supprimer. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/)
