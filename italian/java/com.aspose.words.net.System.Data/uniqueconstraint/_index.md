---
title: "UniqueConstraint"
linktitle: "UniqueConstraint"
second_title: "Aspose.Words per Java"
description: "Rappresenta una restrizione su un insieme di colonne in cui tutti i valori devono essere unici in Java."
type: docs
weight: 32
url: /it/java/com.aspose.words.net.system.data/uniqueconstraint/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Constraint](../../com.aspose.words.net.system.data/constraint/)
```
public class UniqueConstraint extends System.Data.Constraint
```

Rappresenta una restrizione su un insieme di colonne in cui tutti i valori devono essere unici.
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey)](#UniqueConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---boolean) | Inizializza una nuova istanza della classe [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) con il nome specificato, un array di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) da vincolare e un valore che specifica se il vincolo è una chiave primaria. |
| [UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---boolean) | Inizializza una nuova istanza della classe [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) con un array di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) da vincolare e un valore che specifica se il vincolo è una chiave primaria. |
| [UniqueConstraint(System.Data.DataColumn[] columns)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn) | Inizializza una nuova istanza della classe [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) con l'array fornito di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [UniqueConstraint(System.Data.DataColumn column)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn) | Inizializza una nuova istanza della classe [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) con il [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) specificato. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [equals(Object key2)](#equals-java.lang.Object) | Confronta questo vincolo con un secondo per determinare se entrambi sono identici. |
| [getColumns()](#getColumns) | Restituisce l'array di colonne che questo vincolo influenza. |
| [getConstraintName()](#getConstraintName) | Il nome di un vincolo nella [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
| [getTable()](#getTable) | Restituisce la tabella a cui appartiene questo vincolo. |
| [hashCode()](#hashCode) |  |
| [isPrimaryKey()](#isPrimaryKey) | Restituisce un valore che indica se il vincolo è su una chiave primaria. |
| [setConstraintName(String value)](#setConstraintName-java.lang.String) | Il nome di un vincolo nella [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
### UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey) {#UniqueConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---boolean}
```
public UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey)
```


Inizializza una nuova istanza della classe [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) con il nome specificato, un array di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) da vincolare e un valore che specifica se il vincolo è una chiave primaria.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome del vincolo. |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Un array di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) da vincolare. |
| isPrimaryKey | boolean | true per indicare che il vincolo è una chiave primaria; altrimenti false. |

### UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---boolean}
```
public UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey)
```


Inizializza una nuova istanza della classe [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) con un array di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) da vincolare e un valore che specifica se il vincolo è una chiave primaria.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Un array di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) da vincolare. |
| isPrimaryKey | boolean | true per indicare che il vincolo è una chiave primaria; altrimenti false. |

### UniqueConstraint(System.Data.DataColumn[] columns) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn}
```
public UniqueConstraint(System.Data.DataColumn[] columns)
```


Inizializza una nuova istanza della classe [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) con l'array fornito di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | L'array di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) da vincolare. |

### UniqueConstraint(System.Data.DataColumn column) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn}
```
public UniqueConstraint(System.Data.DataColumn column)
```


Inizializza una nuova istanza della classe [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) con il [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Il [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) da vincolare. |

### equals(Object key2) {#equals-java.lang.Object}
```
public boolean equals(Object key2)
```


Confronta questo vincolo con un secondo per determinare se entrambi sono identici.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| key2 | java.lang.Object | L'oggetto con cui questo [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) viene confrontato. |

**Returns:**
boolean - true, se i vincoli sono uguali; altrimenti false.
### getColumns() {#getColumns}
```
public System.Data.DataColumn[] getColumns()
```


Restituisce l'array di colonne che questo vincolo influenza.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Un array di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getConstraintName() {#getConstraintName}
```
public String getConstraintName()
```


Il nome di un vincolo nella [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Returns:**
java.lang.String - Il nome del [Constraint](../../com.aspose.words.net.system.data/constraint/).
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Restituisce la tabella a cui appartiene questo vincolo.

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


Restituisce un valore che indica se il vincolo è su una chiave primaria.

**Returns:**
boolean - true, se il vincolo è su una chiave primaria; altrimenti, false.
### setConstraintName(String value) {#setConstraintName-java.lang.String}
```
public void setConstraintName(String value)
```


Il nome di un vincolo nella [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | java.lang.String | Il nome del [Constraint](../../com.aspose.words.net.system.data/constraint/). |

