---
title: "DataRelationCollection"
linktitle: "DataRelationCollection"
second_title: "Aspose.Words pour Java"
description: "Représente la collection d'objets DataRelation pour cet DataSet en Java."
type: docs
weight: 19
url: /fr/java/com.aspose.words.net.system.data/datarelationcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataRelationCollection implements Iterable
```

Représente la collection d'objets [DataRelation](../../com.aspose.words.net.system.data/datarelation/) pour ce [DataSet](../../com.aspose.words.net.system.data/dataset/).
## Méthodes

| Méthode | Description |
| --- | --- |
| [add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#add-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Crée une [DataRelation](../../com.aspose.words.net.system.data/datarelation/) avec une colonne parent et enfant spécifiées, et l'ajoute à la collection. |
| [add(System.Data.DataRelation relation)](#add-com.aspose.words.net.System.Data.DataRelation) | Ajoute une [DataRelation](../../com.aspose.words.net.system.data/datarelation/) à la [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| [add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName)](#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String-java.lang.String) | Ajoute une relation à la collection. |
| [add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)](#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String) | Ajoute une relation à la collection. |
| [add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Crée une [DataRelation](../../com.aspose.words.net.system.data/datarelation/) avec le nom spécifié, ainsi que les colonnes parent et enfant, et l'ajoute à la collection. |
| [add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)](#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean) | Crée une [DataRelation](../../com.aspose.words.net.system.data/datarelation/) avec le nom spécifié, les colonnes parent et enfant, avec des contraintes facultatives selon la valeur du paramètre  createConstraints , et l'ajoute à la collection. |
| [clear()](#clear) | Efface la collection de toutes les relations. |
| [contains(System.Data.DataRelation relation)](#contains-com.aspose.words.net.System.Data.DataRelation) | Vérifie si une DataRelation avec le nom spécifique (insensible à la casse) existe dans la collection. |
| [get(int index)](#get-int) | Obtient l'objet [DataRelation](../../com.aspose.words.net.system.data/datarelation/) à l'index spécifié. |
| [get(String name)](#get-java.lang.String) | Obtient l'objet [DataRelation](../../com.aspose.words.net.system.data/datarelation/) spécifié par le nom. |
| [getCount()](#getCount) |  |
| [indexOf(System.Data.DataRelation relation)](#indexOf-com.aspose.words.net.System.Data.DataRelation) | Obtient l'index de l'objet [DataRelation](../../com.aspose.words.net.system.data/datarelation/) spécifié. |
| [iterator()](#iterator) |  |
| [removeAt(int index)](#removeAt-int) | Supprime la relation à l'index spécifié de la collection. |
### add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#add-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public void add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Crée une [DataRelation](../../com.aspose.words.net.system.data/datarelation/) avec une colonne parent et enfant spécifiées, et l'ajoute à la collection.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La colonne parent de la relation. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La colonne enfant de la relation. |

### add(System.Data.DataRelation relation) {#add-com.aspose.words.net.System.Data.DataRelation}
```
public void add(System.Data.DataRelation relation)
```


Ajoute une [DataRelation](../../com.aspose.words.net.system.data/datarelation/) à la [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | La DataRelation à ajouter à la collection. |

### add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName) {#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String-java.lang.String}
```
public void add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName)
```


Ajoute une relation à la collection. N'effectue aucune vérification de duplication, etc.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | La table parent de la relation. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | La table enfant de la relation. |
| parentColumnName | java.lang.String | Le nom de la colonne parent de la relation. |
| childColumnName | java.lang.String | Le nom de la colonne enfant de la relation. |

### add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames) {#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String}
```
public void add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)
```


Ajoute une relation à la collection. N'effectue aucune vérification de duplication, etc.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | La table parent de la relation. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | La table enfant de la relation. |
| parentColumnNames | java.lang.String[] | Le tableau des noms des colonnes parent de la relation. |
| childColumnNames | java.lang.String[] | Le tableau des noms des colonnes enfant de la relation. |

### add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public void add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Crée une [DataRelation](../../com.aspose.words.net.system.data/datarelation/) avec le nom spécifié, ainsi que les colonnes parent et enfant, et l'ajoute à la collection.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom de la relation. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La colonne parent de la relation. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La colonne enfant de la relation. |

### add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints) {#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean}
```
public void add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)
```


Crée une [DataRelation](../../com.aspose.words.net.system.data/datarelation/) avec le nom spécifié, les colonnes parent et enfant, avec des contraintes facultatives selon la valeur du paramètre  createConstraints , et l'ajoute à la collection.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom de la relation. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La colonne parent de la relation. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La colonne enfant de la relation. |
| createConstraints | boolean | true pour créer les contraintes ; sinon false. (La valeur par défaut est true). |

### clear() {#clear}
```
public void clear()
```


Efface la collection de toutes les relations.

### contains(System.Data.DataRelation relation) {#contains-com.aspose.words.net.System.Data.DataRelation}
```
public boolean contains(System.Data.DataRelation relation)
```


Vérifie si une DataRelation avec le nom spécifique (insensible à la casse) existe dans la collection.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | Le nom de la relation à rechercher. |

**Returns:**
booléen - true, si une relation avec le nom spécifié existe ; sinon false.
### get(int index) {#get-int}
```
public System.Data.DataRelation get(int index)
```


Obtient l'objet [DataRelation](../../com.aspose.words.net.system.data/datarelation/) à l'index spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | L'index basé sur zéro à rechercher. |

**Returns:**
[DataRelation](../../com.aspose.words.net.system.data/datarelation/) - The [DataRelation](../../com.aspose.words.net.system.data/datarelation/), or a null value if the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/) does not exist.
### get(String name) {#get-java.lang.String}
```
public System.Data.DataRelation get(String name)
```


Obtient l'objet [DataRelation](../../com.aspose.words.net.system.data/datarelation/) spécifié par le nom.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom de la relation à rechercher. |

**Returns:**
[DataRelation](../../com.aspose.words.net.system.data/datarelation/) - The named [DataRelation](../../com.aspose.words.net.system.data/datarelation/), or a null value if the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int - le nombre total d'éléments dans une collection
### indexOf(System.Data.DataRelation relation) {#indexOf-com.aspose.words.net.System.Data.DataRelation}
```
public int indexOf(System.Data.DataRelation relation)
```


Obtient l'index de l'objet [DataRelation](../../com.aspose.words.net.system.data/datarelation/) spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | La relation à rechercher. |

**Returns:**
int - L'index basé sur zéro de la relation, ou -1 si la relation n'est pas trouvée dans la collection.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Supprime la relation à l'index spécifié de la collection.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | L'index de la relation à supprimer. |

