---
title: "ForeignKeyConstraint"
linktitle: "ForeignKeyConstraint"
second_title: "Aspose.Words per Java"
description: "Rappresenta una restrizione d'azione applicata a un insieme di colonne in una relazione chiave primaria/chiave esterna quando un valore o una riga viene eliminato o aggiornato in Java."
type: docs
weight: 29
url: /it/java/com.aspose.words.net.system.data/foreignkeyconstraint/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Constraint](../../com.aspose.words.net.system.data/constraint/)
```
public class ForeignKeyConstraint extends System.Data.Constraint
```

Rappresenta una restrizione d'azione applicata a un insieme di colonne in una relazione chiave primaria/chiave esterna quando un valore o una riga viene eliminato o aggiornato.
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns)](#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn) | Inizializza una nuova istanza della classe [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) con il nome specificato e gli array di [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) genitore e figlio. |
| [ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#ForeignKeyConstraint-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Inizializza una nuova istanza della classe [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) con i [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) genitore e figlio specificati. |
| [ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Inizializza una nuova istanza della classe [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) con il nome, i [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) genitore e figlio specificati. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [equals(Object key)](#equals-java.lang.Object) | Restituisce un valore che indica se l'attuale [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) è identico all'oggetto specificato. |
| [getColumns()](#getColumns) | Restituisce le colonne figlio di questo vincolo. |
| [getConstraintName()](#getConstraintName) | Il nome di un vincolo nella [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
| [getDeleteRule()](#getDeleteRule) | Restituisce l'azione che si verifica su questo vincolo quando una riga viene eliminata. |
| [getRelatedColumns()](#getRelatedColumns) | Le colonne genitore di questo vincolo. |
| [getRelatedTable()](#getRelatedTable) | Restituisce la tabella genitore di questo vincolo. |
| [getTable()](#getTable) | Restituisce la tabella figlio di questo vincolo. |
| [getUpdateRule()](#getUpdateRule) | Restituisce l'azione che si verifica su questo vincolo quando una riga viene aggiornata. |
| [hashCode()](#hashCode) |  |
| [setConstraintName(String value)](#setConstraintName-java.lang.String) | Il nome di un vincolo nella [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
### ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns) {#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns)
```


Inizializza una nuova istanza della classe [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) con il nome specificato e gli array di [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) genitore e figlio.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| constraintName | java.lang.String | Il nome del [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/). Se null o stringa vuota, verrà assegnato un nome predefinito quando viene aggiunto alla raccolta dei vincoli. |
| parentColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Un array di [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) genitore nel vincolo. |
| childColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Un array di [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) figlio nel vincolo. |

### ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#ForeignKeyConstraint-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Inizializza una nuova istanza della classe [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) con i [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) genitore e figlio specificati.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Il [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) genitore nel vincolo. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Il [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) figlio nel vincolo. |

### ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Inizializza una nuova istanza della classe [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) con il nome, i [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) genitore e figlio specificati.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| constraintName | java.lang.String | Il nome del vincolo. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Il [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) genitore nel vincolo. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Il [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) figlio nel vincolo. |

### equals(Object key) {#equals-java.lang.Object}
```
public boolean equals(Object key)
```


Restituisce un valore che indica se l'attuale [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) è identico all'oggetto specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| key | java.lang.Object | L'oggetto a cui viene confrontato questo [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/). Due [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) sono uguali se vincolano le stesse colonne. |

**Returns:**
boolean - true, se gli oggetti sono identici; altrimenti, false.
### getColumns() {#getColumns}
```
public System.Data.DataColumn[] getColumns()
```


Restituisce le colonne figlio di questo vincolo.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Un array di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) che sono le colonne figlio del vincolo.
### getConstraintName() {#getConstraintName}
```
public String getConstraintName()
```


Il nome di un vincolo nella [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Returns:**
java.lang.String - Il nome del [Constraint](../../com.aspose.words.net.system.data/constraint/).
### getDeleteRule() {#getDeleteRule}
```
public System.Data.Rule getDeleteRule()
```


Restituisce l'azione che si verifica su questo vincolo quando una riga viene eliminata.

**Returns:**
[Rule](../../com.aspose.words.net.system.data/rule/) - One of the [Rule](../../com.aspose.words.net.system.data/rule/) values. The default is Cascade. The returned value is one of [Rule](../../com.aspose.words.net.system.data/rule/) constants.
### getRelatedColumns() {#getRelatedColumns}
```
public System.Data.DataColumn[] getRelatedColumns()
```


Le colonne genitore di questo vincolo.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Un array di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) che sono le colonne genitore del vincolo.
### getRelatedTable() {#getRelatedTable}
```
public System.Data.DataTable getRelatedTable()
```


Restituisce la tabella genitore di questo vincolo.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The parent [DataTable](../../com.aspose.words.net.system.data/datatable/) of this constraint.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Restituisce la tabella figlio di questo vincolo.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the child table in the constraint.
### getUpdateRule() {#getUpdateRule}
```
public System.Data.Rule getUpdateRule()
```


Restituisce l'azione che si verifica su questo vincolo quando una riga viene aggiornata.

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


Il nome di un vincolo nella [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | java.lang.String | Il nome del [Constraint](../../com.aspose.words.net.system.data/constraint/). |

