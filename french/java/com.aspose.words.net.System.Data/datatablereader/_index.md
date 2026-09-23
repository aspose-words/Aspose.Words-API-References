---
title: "DataTableReader"
linktitle: "DataTableReader"
second_title: "Aspose.Words pour Java"
description: "Le DataTableReader obtient le contenu d'un ou plusieurs objets DataTable sous la forme d'un ou plusieurs ensembles de résultats en lecture seule, en avant uniquement, en Java."
type: docs
weight: 27
url: /fr/java/com.aspose.words.net.system.data/datatablereader/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Common.DbDataReader](../../com.aspose.words.net.system.data.common/dbdatareader/)
```
public class DataTableReader extends System.Data.Common.DbDataReader
```

Le [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) obtient le contenu d'un ou plusieurs objets [DataTable](../../com.aspose.words.net.system.data/datatable/) sous la forme d'un ou plusieurs ensembles de résultats en lecture seule, en avant uniquement.
## Constructors

| Constructor | Description |
| --- | --- |
| [DataTableReader(System.Data.DataTable dataTable)](#DataTableReader-com.aspose.words.net.System.Data.DataTable) | Initialise une nouvelle instance de la classe [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) en utilisant les données du [DataTable](../../com.aspose.words.net.system.data/datatable/) fourni. |
| [DataTableReader(System.Data.DataTable[] dataTables)](#DataTableReader-com.aspose.words.net.System.Data.DataTable) | Initialise une nouvelle instance de la classe [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) en utilisant le tableau fourni d'objets [DataTable](../../com.aspose.words.net.system.data/datatable/). |
## Méthodes

| Méthode | Description |
| --- | --- |
| [close()](#close) | Ferme le [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) actuel. |
| [get(int ordinal)](#get-int) | Obtient la valeur de la colonne spécifiée dans son format natif à partir de l'indice ordinal de la colonne. |
| [get(String name)](#get-java.lang.String) | Obtient la valeur de la colonne spécifiée dans son format natif à partir du nom de la colonne. |
| [getDepth()](#getDepth) | La profondeur d'imbrication de la ligne actuelle du [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/). |
| [getFieldCount()](#getFieldCount) | Renvoie le nombre de colonnes dans la ligne actuelle. |
| [getFieldType(int ordinal)](#getFieldType-int) | Obtient le java.lang.Class qui est le type de données de l'objet. |
| [getName(int ordinal)](#getName-int) | Obtient la valeur de la colonne spécifiée en tant que java.lang.String. |
| [getRecordsAffected()](#getRecordsAffected) | Obtient le nombre de lignes insérées, modifiées ou supprimées par l'exécution de l'instruction SQL. |
| [getSchemaTable()](#getSchemaTable) | Renvoie un [DataTable](../../com.aspose.words.net.system.data/datatable/) qui décrit les métadonnées des colonnes du [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/). |
| [getValue(int ordinal)](#getValue-int) | Obtient la valeur de la colonne spécifiée dans son format natif. |
| [hasRows()](#hasRows) | Obtient une valeur indiquant si le [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) contient une ou plusieurs lignes. |
| [isClosed()](#isClosed) | Obtient une valeur indiquant si le [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) est fermé. |
| [iterator()](#iterator) | Renvoie un énumérateur pouvant être utilisé pour parcourir la collection d'éléments. |
| [nextResult()](#nextResult) | Fait avancer le [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) vers le jeu de résultats suivant, le cas échéant. |
| [read()](#read) | Fait avancer le [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) vers l'enregistrement suivant. |
### DataTableReader(System.Data.DataTable dataTable) {#DataTableReader-com.aspose.words.net.System.Data.DataTable}
```
public DataTableReader(System.Data.DataTable dataTable)
```


Initialise une nouvelle instance de la classe [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) en utilisant les données du [DataTable](../../com.aspose.words.net.system.data/datatable/) fourni.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Le [DataTable](../../com.aspose.words.net.system.data/datatable/) dont le nouveau [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) obtient son jeu de résultats. |

### DataTableReader(System.Data.DataTable[] dataTables) {#DataTableReader-com.aspose.words.net.System.Data.DataTable}
```
public DataTableReader(System.Data.DataTable[] dataTables)
```


Initialise une nouvelle instance de la classe [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) en utilisant le tableau fourni d'objets [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| dataTables | [DataTable\[\]](../../com.aspose.words.net.system.data/datatable/) | Le tableau d'objets [DataTable](../../com.aspose.words.net.system.data/datatable/) qui fournit les résultats pour le nouvel objet [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/). |

### close() {#close}
```
public void close()
```


Ferme le [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) actuel.

### get(int ordinal) {#get-int}
```
public Object get(int ordinal)
```


Obtient la valeur de la colonne spécifiée dans son format natif à partir de l'indice ordinal de la colonne.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| ordinal | int | L'indice ordinal de la colonne basé sur zéro. |

**Returns:**
java.lang.Object - La valeur de la colonne spécifiée dans son format natif.
### get(String name) {#get-java.lang.String}
```
public Object get(String name)
```


Obtient la valeur de la colonne spécifiée dans son format natif à partir du nom de la colonne.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom de la colonne. |

**Returns:**
java.lang.Object - La valeur de la colonne spécifiée dans son format natif.
### getDepth() {#getDepth}
```
public int getDepth()
```


La profondeur d'imbrication de la ligne actuelle du [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/).

**Returns:**
int - La profondeur d'imbrication de la ligne actuelle ; toujours zéro.
### getFieldCount() {#getFieldCount}
```
public int getFieldCount()
```


Renvoie le nombre de colonnes dans la ligne actuelle.

**Returns:**
int - Lorsqu'il n'est pas positionné sur un jeu de résultats valide, 0 ; sinon le nombre de colonnes dans la ligne actuelle.
### getFieldType(int ordinal) {#getFieldType-int}
```
public Class getFieldType(int ordinal)
```


Obtient le java.lang.Class qui est le type de données de l'objet.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| ordinal | int | L'indice ordinal de la colonne basé sur zéro. |

**Returns:**
java.lang.Class - Le java.lang.Class qui est le type de données de l'objet.
### getName(int ordinal) {#getName-int}
```
public String getName(int ordinal)
```


Obtient la valeur de la colonne spécifiée en tant que java.lang.String.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| ordinal | int | L'indice ordinal de la colonne basé sur zéro |

**Returns:**
java.lang.String - Le nom de la colonne spécifiée.
### getRecordsAffected() {#getRecordsAffected}
```
public int getRecordsAffected()
```


Obtient le nombre de lignes insérées, modifiées ou supprimées par l'exécution de l'instruction SQL.

**Returns:**
int - Le [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) ne prend pas en charge cette propriété et renvoie toujours 0.
### getSchemaTable() {#getSchemaTable}
```
public System.Data.DataTable getSchemaTable()
```


Renvoie un [DataTable](../../com.aspose.words.net.system.data/datatable/) qui décrit les métadonnées des colonnes du [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that describes the column metadata.
### getValue(int ordinal) {#getValue-int}
```
public Object getValue(int ordinal)
```


Obtient la valeur de la colonne spécifiée dans son format natif.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| ordinal | int | L'indice ordinal de la colonne basé sur zéro |

**Returns:**
java.lang.Object - La valeur de la colonne spécifiée. Cette méthode renvoie DBNull pour les colonnes nulles.
### hasRows() {#hasRows}
```
public boolean hasRows()
```


Obtient une valeur indiquant si le [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) contient une ou plusieurs lignes.

**Returns:**
boolean - vrai si le [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) contient une ou plusieurs lignes; sinon faux.
### isClosed() {#isClosed}
```
public boolean isClosed()
```


Obtient une valeur indiquant si le [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) est fermé.

**Returns:**
boolean - Renvoie vrai si le [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) est fermé; sinon, faux.
### iterator() {#iterator}
```
public Iterator iterator()
```


Renvoie un énumérateur pouvant être utilisé pour parcourir la collection d'éléments.

**Returns:**
java.util.Iterator - Un objet java.util.Iterator qui représente la collection d'éléments.
### nextResult() {#nextResult}
```
public boolean nextResult()
```


Fait avancer le [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) vers le jeu de résultats suivant, le cas échéant.

**Returns:**
boolean - vrai s'il y avait un autre jeu de résultats; sinon faux.
### read() {#read}
```
public boolean read()
```


Fait avancer le [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) vers l'enregistrement suivant.

**Returns:**
boolean - vrai s'il y avait une autre ligne à lire; sinon faux.
