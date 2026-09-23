---
title: "UniqueConstraint"
linktitle: "UniqueConstraint"
second_title: "Aspose.Words pour Java"
description: "Représente une restriction sur un ensemble de colonnes dans lequel toutes les valeurs doivent être uniques en Java."
type: docs
weight: 32
url: /fr/java/com.aspose.words.net.system.data/uniqueconstraint/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Constraint](../../com.aspose.words.net.system.data/constraint/)
```
public class UniqueConstraint extends System.Data.Constraint
```

Représente une restriction sur un ensemble de colonnes où toutes les valeurs doivent être uniques.
## Constructors

| Constructor | Description |
| --- | --- |
| [UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey)](#UniqueConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---boolean) | Initialise une nouvelle instance de la classe [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) avec le nom spécifié, un tableau d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) à contraindre, et une valeur indiquant si la contrainte est une clé primaire. |
| [UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---boolean) | Initialise une nouvelle instance de la classe [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) avec un tableau d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) à contraindre, et une valeur indiquant si la contrainte est une clé primaire. |
| [UniqueConstraint(System.Data.DataColumn[] columns)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn) | Initialise une nouvelle instance de la classe [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) avec le tableau donné d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [UniqueConstraint(System.Data.DataColumn column)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn) | Initialise une nouvelle instance de la classe [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) avec le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) spécifié. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [equals(Object key2)](#equals-java.lang.Object) | Compare cette contrainte à une seconde pour déterminer si les deux sont identiques. |
| [getColumns()](#getColumns) | Obtient le tableau de colonnes affectées par cette contrainte. |
| [getConstraintName()](#getConstraintName) | Le nom d'une contrainte dans la [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
| [getTable()](#getTable) | Obtient la table à laquelle cette contrainte appartient. |
| [hashCode()](#hashCode) |  |
| [isPrimaryKey()](#isPrimaryKey) | Obtient une valeur indiquant si la contrainte porte sur une clé primaire ou non. |
| [setConstraintName(String value)](#setConstraintName-java.lang.String) | Le nom d'une contrainte dans la [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
### UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey) {#UniqueConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---boolean}
```
public UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey)
```


Initialise une nouvelle instance de la classe [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) avec le nom spécifié, un tableau d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) à contraindre, et une valeur indiquant si la contrainte est une clé primaire.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom de la contrainte. |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Un tableau d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) à contraindre. |
| isPrimaryKey | boolean | vrai pour indiquer que la contrainte est une clé primaire; sinon, faux. |

### UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---boolean}
```
public UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey)
```


Initialise une nouvelle instance de la classe [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) avec un tableau d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) à contraindre, et une valeur indiquant si la contrainte est une clé primaire.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Un tableau d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) à contraindre. |
| isPrimaryKey | boolean | vrai pour indiquer que la contrainte est une clé primaire; sinon, faux. |

### UniqueConstraint(System.Data.DataColumn[] columns) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn}
```
public UniqueConstraint(System.Data.DataColumn[] columns)
```


Initialise une nouvelle instance de la classe [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) avec le tableau donné d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Le tableau d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) à contraindre. |

### UniqueConstraint(System.Data.DataColumn column) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn}
```
public UniqueConstraint(System.Data.DataColumn column)
```


Initialise une nouvelle instance de la classe [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) avec le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Le [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) à contraindre. |

### equals(Object key2) {#equals-java.lang.Object}
```
public boolean equals(Object key2)
```


Compare cette contrainte à une seconde pour déterminer si les deux sont identiques.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key2 | java.lang.Object | L'objet avec lequel ce [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) est comparé. |

**Returns:**
boolean - vrai, si les contraintes sont égales; sinon, faux.
### getColumns() {#getColumns}
```
public System.Data.DataColumn[] getColumns()
```


Obtient le tableau de colonnes affectées par cette contrainte.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Un tableau d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getConstraintName() {#getConstraintName}
```
public String getConstraintName()
```


Le nom d'une contrainte dans la [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Returns:**
java.lang.String - Le nom de la [Constraint](../../com.aspose.words.net.system.data/constraint/).
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Obtient la table à laquelle cette contrainte appartient.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) to which the constraint belongs.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### isPrimaryKey() {#isPrimaryKey}
```
public boolean isPrimaryKey()
```


Obtient une valeur indiquant si la contrainte porte sur une clé primaire ou non.

**Returns:**
booléen - vrai, si la contrainte porte sur une clé primaire; sinon, faux.
### setConstraintName(String value) {#setConstraintName-java.lang.String}
```
public void setConstraintName(String value)
```


Le nom d'une contrainte dans la [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Le nom de la [Constraint](../../com.aspose.words.net.system.data/constraint/). |

