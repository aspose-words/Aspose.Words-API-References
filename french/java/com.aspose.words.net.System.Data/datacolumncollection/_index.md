---
title: "DataColumnCollection"
linktitle: "DataColumnCollection"
second_title: "Aspose.Words pour Java"
description: "Représente une collection d'objets DataColumn pour un DataTable en Java."
type: docs
weight: 15
url: /fr/java/com.aspose.words.net.system.data/datacolumncollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataColumnCollection implements Iterable
```

Représente une collection d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) pour un [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Méthodes

| Méthode | Description |
| --- | --- |
| [add(System.Data.DataColumn column)](#add-com.aspose.words.net.System.Data.DataColumn) | Crée et ajoute l'objet [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) spécifié à la [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [add(String columnName)](#add-java.lang.String) | Crée et ajoute un objet [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) ayant le nom spécifié à la [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [add(String columnName, Class type)](#add-java.lang.String-java.lang.Class) | Crée et ajoute un objet [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) ayant le nom et le type spécifiés à la [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull)](#add-java.lang.String-java.lang.Class-int-boolean-boolean) | Crée et ajoute un [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) avec le nom, le type et les valeurs spécifiques spécifiés à la collection de colonnes. |
| [clear()](#clear) | Vide la collection de toutes les colonnes. |
| [contains(String name)](#contains-java.lang.String) | Vérifie si la collection contient une colonne avec le nom spécifié. |
| [get(int index)](#get-int) | Obtient le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) de la collection à l'index spécifié. |
| [get(String name)](#get-java.lang.String) | Obtient le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) de la collection avec le nom spécifié. |
| [getCount()](#getCount) |  |
| [indexOf(System.Data.DataColumn column)](#indexOf-com.aspose.words.net.System.Data.DataColumn) | Obtient l'index d'une colonne spécifiée par son nom. |
| [indexOf(String columnName)](#indexOf-java.lang.String) | Obtient l'index de la colonne portant le nom spécifique (le nom n'est pas sensible à la casse). |
| [iterator()](#iterator) |  |
| [remove(System.Data.DataColumn column)](#remove-com.aspose.words.net.System.Data.DataColumn) | Supprime l'objet [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) spécifié de la collection. |
| [remove(String name)](#remove-java.lang.String) | Supprime de la collection l'objet [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) qui possède le nom spécifié. |
### add(System.Data.DataColumn column) {#add-com.aspose.words.net.System.Data.DataColumn}
```
public void add(System.Data.DataColumn column)
```


Crée et ajoute l'objet [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) spécifié à la [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) à ajouter. |

### add(String columnName) {#add-java.lang.String}
```
public void add(String columnName)
```


Crée et ajoute un objet [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) ayant le nom spécifié à la [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String | Le nom de la colonne. |

### add(String columnName, Class type) {#add-java.lang.String-java.lang.Class}
```
public System.Data.DataColumn add(String columnName, Class type)
```


Crée et ajoute un objet [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) ayant le nom et le type spécifiés à la [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String | Le [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) à utiliser lors de la création de la colonne. |
| type | java.lang.Class | Le [DataColumn.getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [DataColumn.setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class) de la nouvelle colonne. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The newly created [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull) {#add-java.lang.String-java.lang.Class-int-boolean-boolean}
```
public System.Data.DataColumn add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull)
```


Crée et ajoute un [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) avec le nom, le type et les valeurs spécifiques spécifiés à la collection de colonnes.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String | nom |
| type | java.lang.Class | type de données |
| columnMapping | int | type de mappage de colonne |
| allowAutoIncrement | boolean | l'auto-incrémentation est autorisée |
| allowDBNull | boolean | la valeur DBNull est autorisée |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - created a [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) instance.
### clear() {#clear}
```
public void clear()
```


Vide la collection de toutes les colonnes.

### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Vérifie si la collection contient une colonne avec le nom spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| name | java.lang.String | Le [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) de la colonne à rechercher. |

**Returns:**
booléen - vrai si une colonne existe avec ce nom ; sinon, faux.
### get(int index) {#get-int}
```
public System.Data.DataColumn get(int index)
```


Obtient le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) de la collection à l'index spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | L'index basé sur zéro de la colonne à retourner. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) at the specified index.
### get(String name) {#get-java.lang.String}
```
public System.Data.DataColumn get(String name)
```


Obtient le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) de la collection avec le nom spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| name | java.lang.String | Le [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) de la colonne à retourner. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in the collection with the specified [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String); otherwise a null value if the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int - le nombre total d'éléments dans une collection.
### indexOf(System.Data.DataColumn column) {#indexOf-com.aspose.words.net.System.Data.DataColumn}
```
public int indexOf(System.Data.DataColumn column)
```


Obtient l'index d'une colonne spécifiée par son nom.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Le nom de la colonne à retourner. |

**Returns:**
int - L'index de la colonne spécifiée par  column  si elle est trouvée ; sinon, -1.
### indexOf(String columnName) {#indexOf-java.lang.String}
```
public int indexOf(String columnName)
```


Obtient l'index de la colonne portant le nom spécifique (le nom n'est pas sensible à la casse).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String | Le nom de la colonne à rechercher. |

**Returns:**
int - L'index basé sur zéro de la colonne avec le nom spécifié, ou -1 si la colonne n'existe pas dans la collection.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(System.Data.DataColumn column) {#remove-com.aspose.words.net.System.Data.DataColumn}
```
public void remove(System.Data.DataColumn column)
```


Supprime l'objet [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) spécifié de la collection.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) à supprimer. |

### remove(String name) {#remove-java.lang.String}
```
public void remove(String name)
```


Supprime de la collection l'objet [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) qui possède le nom spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom de la colonne à supprimer. |

