---
title: "DataTable"
linktitle: "DataTable"
second_title: "Aspose.Words pour Java"
description: "Représente une table de données en mémoire en Java."
type: docs
weight: 25
url: /fr/java/com.aspose.words.net.system.data/datatable/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.net.System.Data.DataTableEventListener](../../com.aspose.words.net.system.data/datatableeventlistener/)
```
public class DataTable implements System.Data.DataTableEventListener
```

Représente une table de données en mémoire.
## Constructors

| Constructor | Description |
| --- | --- |
| [DataTable()](#DataTable) | Initialise une nouvelle instance de la classe [DataTable](../../com.aspose.words.net.system.data/datatable/) sans arguments. |
| [DataTable(String tableName)](#DataTable-java.lang.String) | Initialise une nouvelle instance de la classe [DataTable](../../com.aspose.words.net.system.data/datatable/) avec le nom de table spécifié. |
| [DataTable(ResultSet resultSet)](#DataTable-java.sql.ResultSet) | Crée un objet en encapsulant le ResultSet spécifié. |
| [DataTable(ResultSet resultSet, String tableName)](#DataTable-java.sql.ResultSet-java.lang.String) | Crée un objet en encapsulant le ResultSet spécifié. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [acceptChanges()](#acceptChanges) | Valide toutes les modifications apportées à cette table depuis la dernière fois que [acceptChanges()](../../com.aspose.words.net.system.data/datatable/\#acceptChanges) a été appelée. |
| [addEventListener(System.Data.DataTableEventListener listener)](#addEventListener-com.aspose.words.net.System.Data.DataTableEventListener) |  |
| [clearEventListneers()](#clearEventListneers) |  |
| [close()](#close) |  |
| [containsColumn(String columnName)](#containsColumn-java.lang.String) | Vérifie si la colonne donnée existe ou non |
| [getChildRelations()](#getChildRelations) | Obtient la collection des relations enfants pour ce [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getColumnName(int index)](#getColumnName-int) | Analogue pour .Net DataTable.Columns[i].ColumnName |
| [getColumns()](#getColumns) | Obtient la collection des colonnes appartenant à cette table. |
| [getColumnsCount()](#getColumnsCount) |  |
| [getConstraints()](#getConstraints) | Obtient la collection des contraintes maintenues par cette table. |
| [getDataSet()](#getDataSet) | Obtient le [DataSet](../../com.aspose.words.net.system.data/dataset/) auquel cette table appartient. |
| [getEnforceConstraints()](#getEnforceConstraints) |  |
| [getNamespace()](#getNamespace) | Obtient l'espace de noms pour la représentation XML des données stockées dans le [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getParentRelations()](#getParentRelations) | Obtient la collection des relations parentes pour ce [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getPrimaryKey()](#getPrimaryKey) | Obtient un tableau de colonnes qui fonctionnent comme clés primaires pour la table de données. |
| [getResultSet()](#getResultSet) | Renvoie l'objet ResultSet Java sous-jacent. |
| [getRows()](#getRows) | Obtient la collection des lignes appartenant à cette table. |
| [getTableName()](#getTableName) | Obtient le nom du [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [newRow()](#newRow) | Crée un nouveau [DataRow](../../com.aspose.words.net.system.data/datarow/) avec le même schéma que la table. |
| [onDataColumnDeleted(System.Data.DataColumn column)](#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn) |  |
| [onDataColumnInserted(System.Data.DataColumn column)](#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn) |  |
| [onDataRowChanged(System.Data.DataRow row)](#onDataRowChanged-com.aspose.words.net.System.Data.DataRow) |  |
| [onDataRowDeleted(System.Data.DataRow row)](#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow) |  |
| [onDataRowInserted(System.Data.DataRow row)](#onDataRowInserted-com.aspose.words.net.System.Data.DataRow) |  |
| [refresh()](#refresh) | Recharge toutes les données depuis ResultSet si celui-ci est présent. |
| [setEnforceConstraints(boolean enforceConstraints)](#setEnforceConstraints-boolean) |  |
| [setNamespace(String value)](#setNamespace-java.lang.String) | Définit l'espace de noms pour la représentation XML des données stockées dans le [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [setPrimaryKey(System.Data.DataColumn[] value)](#setPrimaryKey-com.aspose.words.net.System.Data.DataColumn) | Définit un tableau de colonnes qui fonctionnent comme clés primaires pour la table de données. |
| [setTableName(String value)](#setTableName-java.lang.String) | Définit le nom du [DataTable](../../com.aspose.words.net.system.data/datatable/). |
### DataTable() {#DataTable}
```
public DataTable()
```


Initialise une nouvelle instance de la classe [DataTable](../../com.aspose.words.net.system.data/datatable/) sans arguments.

### DataTable(String tableName) {#DataTable-java.lang.String}
```
public DataTable(String tableName)
```


Initialise une nouvelle instance de la classe [DataTable](../../com.aspose.words.net.system.data/datatable/) avec le nom de table spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| tableName | java.lang.String | Le nom à attribuer à la table. Si  tableName  est nul ou une chaîne vide, un nom par défaut est attribué lors de l'ajout à la [DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/). |

### DataTable(ResultSet resultSet) {#DataTable-java.sql.ResultSet}
```
public DataTable(ResultSet resultSet)
```


Crée un objet en enveloppant le ResultSet spécifié. Tente de récupérer le nom de la table à partir des métadonnées de la première colonne du ResultSet.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | ensemble de données |

### DataTable(ResultSet resultSet, String tableName) {#DataTable-java.sql.ResultSet-java.lang.String}
```
public DataTable(ResultSet resultSet, String tableName)
```


Crée un objet en encapsulant le ResultSet spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | ensemble de données |
| tableName | java.lang.String | nom de la table |

### acceptChanges() {#acceptChanges}
```
public void acceptChanges()
```


Valide toutes les modifications apportées à cette table depuis la dernière fois que [acceptChanges()](../../com.aspose.words.net.system.data/datatable/\#acceptChanges) a été appelée.

### addEventListener(System.Data.DataTableEventListener listener) {#addEventListener-com.aspose.words.net.System.Data.DataTableEventListener}
```
public synchronized void addEventListener(System.Data.DataTableEventListener listener)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| listener | [DataTableEventListener](../../com.aspose.words.net.system.data/datatableeventlistener/) |  |

### clearEventListneers() {#clearEventListneers}
```
public synchronized void clearEventListneers()
```




### close() {#close}
```
public void close()
```




### containsColumn(String columnName) {#containsColumn-java.lang.String}
```
public boolean containsColumn(String columnName)
```


Vérifie si la colonne donnée existe ou non

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String | nom de la colonne |

**Returns:**
booléen - `true` si la colonne peut être trouvée avec le `columnName` fourni
### getChildRelations() {#getChildRelations}
```
public System.Data.DataRelationCollection getChildRelations()
```


Obtient la collection des relations enfants pour ce [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains the child relations for the table. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getColumnName(int index) {#getColumnName-int}
```
public String getColumnName(int index)
```


Analogue pour .Net DataTable.Columns[i].ColumnName

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | \- index de la colonne |

**Returns:**
java.lang.String - nom de la colonne par son index.
### getColumns() {#getColumns}
```
public System.Data.DataColumnCollection getColumns()
```


Obtient la collection des colonnes appartenant à cette table.

**Returns:**
[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) - A [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) that contains the collection of [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects for the table. An empty collection is returned if no [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects exist.
### getColumnsCount() {#getColumnsCount}
```
public int getColumnsCount()
```




**Returns:**
int - nombre de colonnes
### getConstraints() {#getConstraints}
```
public System.Data.ConstraintCollection getConstraints()
```


Obtient la collection des contraintes maintenues par cette table.

**Returns:**
[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) - A [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) that contains the collection of [Constraint](../../com.aspose.words.net.system.data/constraint/) objects for the table. An empty collection is returned if no [Constraint](../../com.aspose.words.net.system.data/constraint/) objects exist.
### getDataSet() {#getDataSet}
```
public System.Data.DataSet getDataSet()
```


Obtient le [DataSet](../../com.aspose.words.net.system.data/dataset/) auquel cette table appartient.

**Returns:**
[DataSet](../../com.aspose.words.net.system.data/dataset/) - The [DataSet](../../com.aspose.words.net.system.data/dataset/) to which this table belongs.
### getEnforceConstraints() {#getEnforceConstraints}
```
public boolean getEnforceConstraints()
```




**Returns:**
boolean - indicateur qui indique si la contrainte de vérification est violée ou non
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


Obtient l'espace de noms pour la représentation XML des données stockées dans le [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
java.lang.String - L'espace de noms du [DataTable](../../com.aspose.words.net.system.data/datatable/).
### getParentRelations() {#getParentRelations}
```
public System.Data.DataRelationCollection getParentRelations()
```


Obtient la collection des relations parentes pour ce [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains the parent relations for the table. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getPrimaryKey() {#getPrimaryKey}
```
public System.Data.DataColumn[] getPrimaryKey()
```


Obtient un tableau de colonnes qui fonctionnent comme clés primaires pour la table de données.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Un tableau d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getResultSet() {#getResultSet}
```
public ResultSet getResultSet()
```


Renvoie l'objet ResultSet Java sous-jacent. Idéalement, nous aimerions travailler avec DataTable de manière .Net. Mais certains utilisateurs et même certains de nos exemples de code utilisent cette propriété.

**Returns:**
java.sql.ResultSet - le java.sql.ResultSet sous-jacent
### getRows() {#getRows}
```
public System.Data.DataRowCollection getRows()
```


Obtient la collection des lignes appartenant à cette table.

**Returns:**
[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) - A [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) that contains [DataRow](../../com.aspose.words.net.system.data/datarow/) objects; otherwise a null value if no [DataRow](../../com.aspose.words.net.system.data/datarow/) objects exist.
### getTableName() {#getTableName}
```
public String getTableName()
```


Obtient le nom du [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
java.lang.String - Le nom du [DataTable](../../com.aspose.words.net.system.data/datatable/).
### newRow() {#newRow}
```
public System.Data.DataRow newRow()
```


Crée un nouveau [DataRow](../../com.aspose.words.net.system.data/datarow/) avec le même schéma que la table.

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A [DataRow](../../com.aspose.words.net.system.data/datarow/) with the same schema as the [DataTable](../../com.aspose.words.net.system.data/datatable/).
### onDataColumnDeleted(System.Data.DataColumn column) {#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn}
```
public void onDataColumnDeleted(System.Data.DataColumn column)
```


Mettre à jour l'écouteur lorsque DataColumn est supprimé

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) |  |

### onDataColumnInserted(System.Data.DataColumn column) {#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn}
```
public void onDataColumnInserted(System.Data.DataColumn column)
```


Mettre à jour l'écouteur lorsque DataColumn est inséré

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) |  |

### onDataRowChanged(System.Data.DataRow row) {#onDataRowChanged-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowChanged(System.Data.DataRow row)
```


Mettre à jour l'écouteur lorsque DataRow est modifié

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### onDataRowDeleted(System.Data.DataRow row) {#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowDeleted(System.Data.DataRow row)
```


Mettre à jour l'écouteur lorsque DataRow est supprimé

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### onDataRowInserted(System.Data.DataRow row) {#onDataRowInserted-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowInserted(System.Data.DataRow row)
```


Mettre à jour l'écouteur lorsque la DataRow est insérée

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### refresh() {#refresh}
```
public void refresh()
```


Recharge toutes les données depuis ResultSet si celui-ci est présent.

### setEnforceConstraints(boolean enforceConstraints) {#setEnforceConstraints-boolean}
```
public void setEnforceConstraints(boolean enforceConstraints)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| enforceConstraints | boolean | est l'indicateur qui indique si la contrainte de vérification est violée ou non |

### setNamespace(String value) {#setNamespace-java.lang.String}
```
public void setNamespace(String value)
```


Définit l'espace de noms pour la représentation XML des données stockées dans le [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | java.lang.String | L'espace de noms du [DataTable](../../com.aspose.words.net.system.data/datatable/). |

### setPrimaryKey(System.Data.DataColumn[] value) {#setPrimaryKey-com.aspose.words.net.System.Data.DataColumn}
```
public void setPrimaryKey(System.Data.DataColumn[] value)
```


Définit un tableau de colonnes qui fonctionnent comme clés primaires pour la table de données.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Un tableau d'objets [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |

### setTableName(String value) {#setTableName-java.lang.String}
```
public void setTableName(String value)
```


Définit le nom du [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Le nom du [DataTable](../../com.aspose.words.net.system.data/datatable/). |

