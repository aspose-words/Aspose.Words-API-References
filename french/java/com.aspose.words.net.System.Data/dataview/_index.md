---
title: "DataView"
linktitle: "DataView"
second_title: "Aspose.Words pour Java"
description: "Représente une vue personnalisée liée aux données d'un DataTable pour le tri, le filtrage, la recherche, la modification et la navigation en Java."
type: docs
weight: 28
url: /fr/java/com.aspose.words.net.system.data/dataview/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataView implements Iterable
```

Représente une vue personnalisée, liée aux données, d'un [DataTable](../../com.aspose.words.net.system.data/datatable/) pour le tri, le filtrage, la recherche, la modification et la navigation.
## Constructors

| Constructor | Description |
| --- | --- |
| [DataView(System.Data.DataTable table)](#DataView-com.aspose.words.net.System.Data.DataTable) | Initialise une nouvelle instance de la classe [DataView](../../com.aspose.words.net.system.data/dataview/) avec le [DataTable](../../com.aspose.words.net.system.data/datatable/) spécifié. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [close()](#close) | Ferme le [DataView](../../com.aspose.words.net.system.data/dataview/). |
| [get(int recordIndex)](#get-int) | Obtient une ligne de données d'une table spécifiée. |
| [getCount()](#getCount) | Obtient le nombre d'enregistrements dans le [DataView](../../com.aspose.words.net.system.data/dataview/). |
| [getTable()](#getTable) | Obtient le [DataTable](../../com.aspose.words.net.system.data/datatable/) source. |
| [iterator()](#iterator) | Obtient un énumérateur pour ce [DataView](../../com.aspose.words.net.system.data/dataview/). |
### DataView(System.Data.DataTable table) {#DataView-com.aspose.words.net.System.Data.DataTable}
```
public DataView(System.Data.DataTable table)
```


Initialise une nouvelle instance de la classe [DataView](../../com.aspose.words.net.system.data/dataview/) avec le [DataTable](../../com.aspose.words.net.system.data/datatable/) spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Un [DataTable](../../com.aspose.words.net.system.data/datatable/) à ajouter au [DataView](../../com.aspose.words.net.system.data/dataview/). |

### close() {#close}
```
public void close()
```


Ferme le [DataView](../../com.aspose.words.net.system.data/dataview/).

### get(int recordIndex) {#get-int}
```
public System.Data.DataRowView get(int recordIndex)
```


Obtient une ligne de données d'une table spécifiée.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| recordIndex | int | L'index d'un enregistrement dans le [DataTable](../../com.aspose.words.net.system.data/datatable/). |

**Returns:**
[DataRowView](../../com.aspose.words.net.system.data/datarowview/) - A [DataRowView](../../com.aspose.words.net.system.data/datarowview/) of the row that you want.
### getCount() {#getCount}
```
public int getCount()
```


Obtient le nombre d'enregistrements dans le [DataView](../../com.aspose.words.net.system.data/dataview/).

**Returns:**
int - Le nombre d'enregistrements dans le [DataView](../../com.aspose.words.net.system.data/dataview/).
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Obtient le [DataTable](../../com.aspose.words.net.system.data/datatable/) source.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that provides the data for this view.
### iterator() {#iterator}
```
public Iterator iterator()
```


Obtient un énumérateur pour ce [DataView](../../com.aspose.words.net.system.data/dataview/).

**Returns:**
java.util.Iterator - Un java.util.Iterator pour naviguer dans la liste.
