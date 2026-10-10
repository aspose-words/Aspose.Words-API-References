---
title: "DataRow"
linktitle: "DataRow"
second_title: "Aspose.Words pour Java"
description: "Représente une ligne de données dans un DataTable en Java."
type: docs
weight: 20
url: /fr/java/com.aspose.words.net.system.data/datarow/
---

**Inheritance:**
java.lang.Object
```
public class DataRow
```

Représente une ligne de données dans un [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Méthodes

| Méthode | Description |
| --- | --- |
| [delete()](#delete) | Supprime le [DataRow](../../com.aspose.words.net.system.data/datarow/). |
| [get(System.Data.DataColumn column)](#get-com.aspose.words.net.System.Data.DataColumn) | Obtient les données stockées dans le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) spécifié. |
| [get(int columnIndex)](#get-int) | Obtient les données stockées dans la colonne spécifiée par l'index. |
| [get(String columnName)](#get-java.lang.String) | Obtient les données stockées dans la colonne spécifiée par le nom. |
| [getChildRows(System.Data.DataRelation relation)](#getChildRows-com.aspose.words.net.System.Data.DataRelation) | Obtient les lignes enfants de ce [DataRow](../../com.aspose.words.net.system.data/datarow/) en utilisant la [DataRelation](../../com.aspose.words.net.system.data/datarelation/) spécifiée. |
| [getItemArray()](#getItemArray) | Obtient toutes les valeurs de cette ligne via un tableau. |
| [getKeyValues(System.Data.DataKey childKey)](#getKeyValues-com.aspose.words.net.System.Data.DataKey) |  |
| [getOriginalValue(String columnName)](#getOriginalValue-java.lang.String) |  |
| [getParentRow(System.Data.DataRelation relation)](#getParentRow-com.aspose.words.net.System.Data.DataRelation) | Obtient la ligne parent d'un [DataRow](../../com.aspose.words.net.system.data/datarow/) en utilisant la [DataRelation](../../com.aspose.words.net.system.data/datarelation/) spécifiée. |
| [getParentRows(System.Data.DataRelation relation)](#getParentRows-com.aspose.words.net.System.Data.DataRelation) | Obtient les lignes parentes d'un [DataRow](../../com.aspose.words.net.system.data/datarow/) en utilisant la [DataRelation](../../com.aspose.words.net.system.data/datarelation/) spécifiée. |
| [getRowState()](#getRowState) | Obtient l'état actuel de la ligne par rapport à sa relation avec le [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/). |
| [getTable()](#getTable) | Obtient le [DataTable](../../com.aspose.words.net.system.data/datatable/) pour lequel cette ligne possède un schéma. |
| [readFrom(ResultSet resultSet)](#readFrom-java.sql.ResultSet) | Lit les valeurs du java.sql.ResultSet |
| [remove(int index)](#remove-int) |  |
| [set(System.Data.DataColumn column, Object value)](#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object) | Définit les données stockées dans le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) spécifié. |
| [set(int columnIndex, Object value)](#set-int-java.lang.Object) | Définit les données stockées dans la colonne spécifiée par l'index. |
| [set(String columnName, Object value)](#set-java.lang.String-java.lang.Object) | Définit les données stockées dans la colonne spécifiée par le nom. |
| [setItemArray(Object[] value)](#setItemArray-java.lang.Object) | Définit toutes les valeurs de cette ligne via un tableau. |
| [setOriginalValue(String columnName, Object data)](#setOriginalValue-java.lang.String-java.lang.Object) |  |
| [setRowState(int state)](#setRowState-int) |  |
| [toString()](#toString) |  |
### delete() {#delete}
```
public void delete()
```


Supprime le [DataRow](../../com.aspose.words.net.system.data/datarow/).

### get(System.Data.DataColumn column) {#get-com.aspose.words.net.System.Data.DataColumn}
```
public Object get(System.Data.DataColumn column)
```


Obtient les données stockées dans le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Un [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) qui contient les données. |

**Returns:**
java.lang.Object - Un java.lang.Object qui contient les données.
### get(int columnIndex) {#get-int}
```
public Object get(int columnIndex)
```


Obtient les données stockées dans la colonne spécifiée par l'index.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| columnIndex | int | L'index zéro‑basé de la colonne. |

**Returns:**
java.lang.Object - Un java.lang.Object qui contient les données.
### get(String columnName) {#get-java.lang.String}
```
public Object get(String columnName)
```


Obtient les données stockées dans la colonne spécifiée par le nom.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String | Le nom de la colonne. |

**Returns:**
java.lang.Object - Un java.lang.Object qui contient les données.
### getChildRows(System.Data.DataRelation relation) {#getChildRows-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow[] getChildRows(System.Data.DataRelation relation)
```


Obtient les lignes enfants de ce [DataRow](../../com.aspose.words.net.system.data/datarow/) en utilisant la [DataRelation](../../com.aspose.words.net.system.data/datarelation/) spécifiée.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | La [DataRelation](../../com.aspose.words.net.system.data/datarelation/) à utiliser. |

**Returns:**
com.aspose.words.net.System.Data.DataRow[] - Un tableau d'objets [DataRow](../../com.aspose.words.net.system.data/datarow/) ou un tableau de longueur zéro.
### getItemArray() {#getItemArray}
```
public Object[] getItemArray()
```


Obtient toutes les valeurs de cette ligne via un tableau.

**Returns:**
java.lang.Object[] - Un tableau du type java.lang.Object.
### getKeyValues(System.Data.DataKey childKey) {#getKeyValues-com.aspose.words.net.System.Data.DataKey}
```
public Object[] getKeyValues(System.Data.DataKey childKey)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| childKey | [DataKey](../../com.aspose.words.net.system.data/datakey/) |  |

**Returns:**
java.lang.Object[]
### getOriginalValue(String columnName) {#getOriginalValue-java.lang.String}
```
public Object getOriginalValue(String columnName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String |  |

**Returns:**
java.lang.Object
### getParentRow(System.Data.DataRelation relation) {#getParentRow-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow getParentRow(System.Data.DataRelation relation)
```


Obtient la ligne parent d'un [DataRow](../../com.aspose.words.net.system.data/datarow/) en utilisant la [DataRelation](../../com.aspose.words.net.system.data/datarelation/) spécifiée.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | La [DataRelation](../../com.aspose.words.net.system.data/datarelation/) à utiliser. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - The parent [DataRow](../../com.aspose.words.net.system.data/datarow/) of the current row.
### getParentRows(System.Data.DataRelation relation) {#getParentRows-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow[] getParentRows(System.Data.DataRelation relation)
```


Obtient les lignes parentes d'un [DataRow](../../com.aspose.words.net.system.data/datarow/) en utilisant la [DataRelation](../../com.aspose.words.net.system.data/datarelation/) spécifiée.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | La [DataRelation](../../com.aspose.words.net.system.data/datarelation/) à utiliser. |

**Returns:**
com.aspose.words.net.System.Data.DataRow[] - Un tableau d'objets [DataRow](../../com.aspose.words.net.system.data/datarow/) ou un tableau de longueur zéro.
### getRowState() {#getRowState}
```
public int getRowState()
```


Obtient l'état actuel de la ligne par rapport à sa relation avec le [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).

**Returns:**
int - L'une des valeurs de [DataRowState](../../com.aspose.words.net.system.data/datarowstate/) . La valeur retournée est une combinaison binaire des constantes de [DataRowState](../../com.aspose.words.net.system.data/datarowstate/).
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Obtient le [DataTable](../../com.aspose.words.net.system.data/datatable/) pour lequel cette ligne possède un schéma.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) to which this row belongs.
### readFrom(ResultSet resultSet) {#readFrom-java.sql.ResultSet}
```
public boolean readFrom(ResultSet resultSet)
```


Lit les valeurs du java.sql.ResultSet

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | stockage à lire |

**Returns:**
booléen - vrai si aucune erreur de lecture ne s'est produite
### remove(int index) {#remove-int}
```
public void remove(int index)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int |  |

### set(System.Data.DataColumn column, Object value) {#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object}
```
public void set(System.Data.DataColumn column, Object value)
```


Définit les données stockées dans le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Un [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) qui contient les données. |
| valeur | java.lang.Object | Un java.lang.Object qui contient les données. |

### set(int columnIndex, Object value) {#set-int-java.lang.Object}
```
public void set(int columnIndex, Object value)
```


Définit les données stockées dans la colonne spécifiée par l'index.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| columnIndex | int | L'index zéro‑basé de la colonne. |
| valeur | java.lang.Object | Un java.lang.Object qui contient les données. |

### set(String columnName, Object value) {#set-java.lang.String-java.lang.Object}
```
public void set(String columnName, Object value)
```


Définit les données stockées dans la colonne spécifiée par le nom.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String | Le nom de la colonne. |
| valeur | java.lang.Object | Un java.lang.Object qui contient les données. |

### setItemArray(Object[] value) {#setItemArray-java.lang.Object}
```
public void setItemArray(Object[] value)
```


Définit toutes les valeurs de cette ligne via un tableau.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.Object[] | Un tableau de type java.lang.Object. |

### setOriginalValue(String columnName, Object data) {#setOriginalValue-java.lang.String-java.lang.Object}
```
public void setOriginalValue(String columnName, Object data)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String |  |
| données | java.lang.Object |  |

### setRowState(int state) {#setRowState-int}
```
public void setRowState(int state)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| état | int |  |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
