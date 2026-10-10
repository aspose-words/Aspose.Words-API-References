---
title: "ForeignKeyConstraint"
linktitle: "ForeignKeyConstraint"
second_title: "Aspose.Words pour Java"
description: "Représente une restriction d'action appliquée à un ensemble de colonnes dans une relation clé primaire/clé étrangère lorsqu'une valeur ou une ligne est supprimée ou mise à jour en Java."
type: docs
weight: 29
url: /fr/java/com.aspose.words.net.system.data/foreignkeyconstraint/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Constraint](../../com.aspose.words.net.system.data/constraint/)
```
public class ForeignKeyConstraint extends System.Data.Constraint
```

Représente une restriction d'action appliquée à un ensemble de colonnes dans une relation clé primaire/clé étrangère lorsqu'une valeur ou une ligne est supprimée ou mise à jour.
## Constructors

| Constructor | Description |
| --- | --- |
| [ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns)](#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn) | Initialise une nouvelle instance de la classe [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) avec le nom spécifié, ainsi que des tableaux de [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) parents et enfants. |
| [ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#ForeignKeyConstraint-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Initialise une nouvelle instance de la classe [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) avec les [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) parents et enfants spécifiés. |
| [ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Initialise une nouvelle instance de la classe [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) avec le nom, les [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) parents et enfants spécifiés. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [equals(Object key)](#equals-java.lang.Object) | Obtient une valeur indiquant si le [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) actuel est identique à l'objet spécifié. |
| [getColumns()](#getColumns) | Obtient les colonnes enfants de cette contrainte. |
| [getConstraintName()](#getConstraintName) | Le nom d'une contrainte dans la [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
| [getDeleteRule()](#getDeleteRule) | Obtient l'action qui se produit sur cette contrainte lorsqu'une ligne est supprimée. |
| [getRelatedColumns()](#getRelatedColumns) | Les colonnes parentes de cette contrainte. |
| [getRelatedTable()](#getRelatedTable) | Obtient la table parente de cette contrainte. |
| [getTable()](#getTable) | Obtient la table enfant de cette contrainte. |
| [getUpdateRule()](#getUpdateRule) | Obtient l'action qui se produit sur cette contrainte lorsqu'une ligne est mise à jour. |
| [hashCode()](#hashCode) |  |
| [setConstraintName(String value)](#setConstraintName-java.lang.String) | Le nom d'une contrainte dans la [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
### ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns) {#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns)
```


Initialise une nouvelle instance de la classe [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) avec le nom spécifié, ainsi que des tableaux de [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) parents et enfants.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| constraintName | java.lang.String | Le nom du [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/). Si null ou chaîne vide, un nom par défaut sera attribué lors de l'ajout à la collection de contraintes. |
| parentColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Un tableau de [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) parents dans la contrainte. |
| childColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Un tableau de [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) enfants dans la contrainte. |

### ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#ForeignKeyConstraint-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Initialise une nouvelle instance de la classe [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) avec les [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) parents et enfants spécifiés.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) parent dans la contrainte. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) enfant dans la contrainte. |

### ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Initialise une nouvelle instance de la classe [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) avec le nom, les [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) parents et enfants spécifiés.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| constraintName | java.lang.String | Le nom de la contrainte. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) parent dans la contrainte. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) enfant dans la contrainte. |

### equals(Object key) {#equals-java.lang.Object}
```
public boolean equals(Object key)
```


Obtient une valeur indiquant si le [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) actuel est identique à l'objet spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | java.lang.Object | L'objet auquel ce [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) est comparé. Deux [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) sont égaux s'ils contraignent les mêmes colonnes. |

**Returns:**
booléen - vrai, si les objets sont identiques ; sinon, faux.
### getColumns() {#getColumns}
```
public System.Data.DataColumn[] getColumns()
```


Obtient les colonnes enfants de cette contrainte.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Un tableau d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) qui sont les colonnes enfants de la contrainte.
### getConstraintName() {#getConstraintName}
```
public String getConstraintName()
```


Le nom d'une contrainte dans la [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Returns:**
java.lang.String - Le nom de la [Constraint](../../com.aspose.words.net.system.data/constraint/).
### getDeleteRule() {#getDeleteRule}
```
public System.Data.Rule getDeleteRule()
```


Obtient l'action qui se produit sur cette contrainte lorsqu'une ligne est supprimée.

**Returns:**
[Rule](../../com.aspose.words.net.system.data/rule/) - One of the [Rule](../../com.aspose.words.net.system.data/rule/) values. The default is Cascade. The returned value is one of [Rule](../../com.aspose.words.net.system.data/rule/) constants.
### getRelatedColumns() {#getRelatedColumns}
```
public System.Data.DataColumn[] getRelatedColumns()
```


Les colonnes parentes de cette contrainte.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Un tableau d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) qui sont les colonnes parentes de la contrainte.
### getRelatedTable() {#getRelatedTable}
```
public System.Data.DataTable getRelatedTable()
```


Obtient la table parente de cette contrainte.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The parent [DataTable](../../com.aspose.words.net.system.data/datatable/) of this constraint.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Obtient la table enfant de cette contrainte.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the child table in the constraint.
### getUpdateRule() {#getUpdateRule}
```
public System.Data.Rule getUpdateRule()
```


Obtient l'action qui se produit sur cette contrainte lorsqu'une ligne est mise à jour.

**Returns:**
[Rule](../../com.aspose.words.net.system.data/rule/) - One of the [Rule](../../com.aspose.words.net.system.data/rule/) values. The default is Cascade. The returned value is one of [Rule](../../com.aspose.words.net.system.data/rule/) constants.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### setConstraintName(String value) {#setConstraintName-java.lang.String}
```
public void setConstraintName(String value)
```


Le nom d'une contrainte dans la [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Le nom de la [Constraint](../../com.aspose.words.net.system.data/constraint/). |

