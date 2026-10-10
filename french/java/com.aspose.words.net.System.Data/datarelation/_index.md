---
title: "DataRelation"
linktitle: "DataRelation"
second_title: "Aspose.Words pour Java"
description: "Représente une relation parent/enfant entre deux objets DataTable en Java."
type: docs
weight: 18
url: /fr/java/com.aspose.words.net.system.data/datarelation/
---

**Inheritance:**
java.lang.Object
```
public class DataRelation
```

Représente une relation parent/enfant entre deux objets [DataTable](../../com.aspose.words.net.system.data/datatable/) .
## Constructors

| Constructor | Description |
| --- | --- |
| [DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String) | Initialise une nouvelle instance de la classe [DataRelation](../../com.aspose.words.net.system.data/datarelation/) en utilisant le nom spécifié, les tables parent et enfant, ainsi que les tableaux correspondants de colonnes parent et enfant. |
| [DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---boolean) | Initialise une nouvelle instance de la classe [DataRelation](../../com.aspose.words.net.system.data/datarelation/) en utilisant le nom spécifié, les tableaux correspondants d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) parent et enfant, et une valeur indiquant s'il faut créer des contraintes. |
| [DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean) | Initialise une nouvelle instance de la classe [DataRelation](../../com.aspose.words.net.system.data/datarelation/) en utilisant le nom spécifié, les objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) parent et enfant, et une valeur indiquant s'il faut créer des contraintes. |
| [DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Initialise une nouvelle instance de la classe [DataRelation](../../com.aspose.words.net.system.data/datarelation/) en utilisant le nom [DataRelation](../../com.aspose.words.net.system.data/datarelation/) spécifié, ainsi que les objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) parent et enfant. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) |  |
| [getChildColumnNames()](#getChildColumnNames) |  |
| [getChildColumns()](#getChildColumns) | Obtient les objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) enfants de cette relation. |
| [getChildKey()](#getChildKey) |  |
| [getChildKeyConstraint()](#getChildKeyConstraint) | Obtient le [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) pour la relation. |
| [getChildTable()](#getChildTable) | Obtient la table enfant de cette relation. |
| [getChildTableName()](#getChildTableName) |  |
| [getDataSet()](#getDataSet) | Obtient le [DataSet](../../com.aspose.words.net.system.data/dataset/) auquel appartient le [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getParentColumnNames()](#getParentColumnNames) |  |
| [getParentColumns()](#getParentColumns) | Obtient un tableau d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) qui sont les colonnes parent de ce [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getParentKey()](#getParentKey) |  |
| [getParentKeyConstraint()](#getParentKeyConstraint) | Obtient le [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) qui garantit que les valeurs de la colonne parent d'un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sont uniques. |
| [getParentTable()](#getParentTable) | Obtient le [DataTable](../../com.aspose.words.net.system.data/datatable/) parent de ce [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getParentTableName()](#getParentTableName) |  |
| [getRelationName()](#getRelationName) | Obtient le nom utilisé pour récupérer un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) depuis le [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| [hashCode()](#hashCode) |  |
| [setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint)](#setChildKeyConstraint-com.aspose.words.net.System.Data.ForeignKeyConstraint) |  |
| [setNested(boolean value)](#setNested-boolean) | Définit une valeur indiquant si les objets [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sont imbriqués. |
| [setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint)](#setParentKeyConstraint-com.aspose.words.net.System.Data.UniqueConstraint) |  |
### DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String}
```
public DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)
```


Initialise une nouvelle instance de la classe [DataRelation](../../com.aspose.words.net.system.data/datarelation/) en utilisant le nom spécifié, les tables parent et enfant, ainsi que les tableaux correspondants de colonnes parent et enfant.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| relationName | java.lang.String | Le nom du DataRelation. S'il est nul ou une chaîne vide (""), un nom par défaut sera attribué lorsque l'objet créé sera ajouté à la DataRelationCollection. |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | La table parent dans la relation. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | La table enfant dans la relation. |
| parentColumnNames | java.lang.String[] | Le nom du DataColumn parent dans la relation. |
| childColumnNames | java.lang.String[] | Le DataColumn enfant dans la relation. |

### DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---boolean}
```
public DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints)
```


Initialise une nouvelle instance de la classe [DataRelation](../../com.aspose.words.net.system.data/datarelation/) en utilisant le nom spécifié, les tableaux correspondants d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) parent et enfant, et une valeur indiquant s'il faut créer des contraintes.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| relationName | java.lang.String | Le nom de la relation. Si null ou une chaîne vide (""), un nom par défaut sera attribué lorsque l'objet créé sera ajouté à la [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| parentColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Un tableau d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) parents. |
| childColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Un tableau d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) enfants. |
| createConstraints | boolean | Une valeur indiquant s'il faut créer des contraintes. true, si les contraintes sont créées. Sinon, false. |

### DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean}
```
public DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)
```


Initialise une nouvelle instance de la classe [DataRelation](../../com.aspose.words.net.system.data/datarelation/) en utilisant le nom spécifié, les objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) parent et enfant, et une valeur indiquant s'il faut créer des contraintes.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| relationName | java.lang.String | Le nom de la relation. Si null ou une chaîne vide (""), un nom par défaut sera attribué lorsque l'objet créé sera ajouté à la [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) parent dans la relation. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) enfant dans la relation. |
| createConstraints | boolean | Une valeur indiquant si les contraintes sont créées. true, si les contraintes sont créées. Sinon, false. |

### DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Initialise une nouvelle instance de la classe [DataRelation](../../com.aspose.words.net.system.data/datarelation/) en utilisant le nom [DataRelation](../../com.aspose.words.net.system.data/datarelation/) spécifié, ainsi que les objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) parent et enfant.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| relationName | java.lang.String | Le nom du [DataRelation](../../com.aspose.words.net.system.data/datarelation/). Si null ou une chaîne vide (""), un nom par défaut sera attribué lorsque l'objet créé sera ajouté à la [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) parent dans la relation. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) enfant dans la relation. |

### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getChildColumnNames() {#getChildColumnNames}
```
public String[] getChildColumnNames()
```




**Returns:**
java.lang.String[] - les noms des DataColumn enfants de cette relation.
### getChildColumns() {#getChildColumns}
```
public System.Data.DataColumn[] getChildColumns()
```


Obtient les objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) enfants de cette relation.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Un tableau d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getChildKey() {#getChildKey}
```
public System.Data.DataKey getChildKey()
```




**Returns:**
[DataKey](../../com.aspose.words.net.system.data/datakey/)
### getChildKeyConstraint() {#getChildKeyConstraint}
```
public System.Data.ForeignKeyConstraint getChildKeyConstraint()
```


Obtient le [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) pour la relation.

**Returns:**
[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) - A [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/).
### getChildTable() {#getChildTable}
```
public System.Data.DataTable getChildTable()
```


Obtient la table enfant de cette relation.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the child table of the relation.
### getChildTableName() {#getChildTableName}
```
public String getChildTableName()
```




**Returns:**
java.lang.String - le nom du DataTable enfant de ce DataRelation.
### getDataSet() {#getDataSet}
```
public System.Data.DataSet getDataSet()
```


Obtient le [DataSet](../../com.aspose.words.net.system.data/dataset/) auquel appartient le [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Returns:**
[DataSet](../../com.aspose.words.net.system.data/dataset/) - A [DataSet](../../com.aspose.words.net.system.data/dataset/) to which the [DataRelation](../../com.aspose.words.net.system.data/datarelation/) belongs.
### getParentColumnNames() {#getParentColumnNames}
```
public String[] getParentColumnNames()
```




**Returns:**
java.lang.String[] - les noms des DataColumn parents de cette relation.
### getParentColumns() {#getParentColumns}
```
public System.Data.DataColumn[] getParentColumns()
```


Obtient un tableau d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) qui sont les colonnes parent de ce [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Un tableau d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) qui sont les colonnes parentes de ce [DataRelation](../../com.aspose.words.net.system.data/datarelation/).
### getParentKey() {#getParentKey}
```
public System.Data.DataKey getParentKey()
```




**Returns:**
[DataKey](../../com.aspose.words.net.system.data/datakey/)
### getParentKeyConstraint() {#getParentKeyConstraint}
```
public System.Data.UniqueConstraint getParentKeyConstraint()
```


Obtient le [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) qui garantit que les valeurs de la colonne parent d'un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sont uniques.

**Returns:**
[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) - A [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) that makes sure that values in a parent column are unique.
### getParentTable() {#getParentTable}
```
public System.Data.DataTable getParentTable()
```


Obtient le [DataTable](../../com.aspose.words.net.system.data/datatable/) parent de ce [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the parent table of this relation.
### getParentTableName() {#getParentTableName}
```
public String getParentTableName()
```




**Returns:**
java.lang.String - le nom du DataTable parent de ce DataRelation.
### getRelationName() {#getRelationName}
```
public String getRelationName()
```


Obtient le nom utilisé pour récupérer un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) depuis le [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/).

**Returns:**
java.lang.String - Le nom d'un [DataRelation](../../com.aspose.words.net.system.data/datarelation/).
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint) {#setChildKeyConstraint-com.aspose.words.net.System.Data.ForeignKeyConstraint}
```
public void setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| childKeyConstraint | [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) |  |

### setNested(boolean value) {#setNested-boolean}
```
public void setNested(boolean value)
```


Définit une valeur indiquant si les objets [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sont imbriqués.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | boolean | true, si les objets [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sont imbriqués ; sinon, false. |

### setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint) {#setParentKeyConstraint-com.aspose.words.net.System.Data.UniqueConstraint}
```
public void setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| parentKeyConstraint | [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) |  |

