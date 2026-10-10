---
title: "DataRelation"
linktitle: "DataRelation"
second_title: "Aspose.Words per Java"
description: "Rappresenta una relazione genitore/figlio tra due oggetti DataTable in Java."
type: docs
weight: 18
url: /it/java/com.aspose.words.net.system.data/datarelation/
---

**Inheritance:**
java.lang.Object
```
public class DataRelation
```

Rappresenta una relazione genitore/figlio tra due oggetti [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String) | Inizializza una nuova istanza della classe [DataRelation](../../com.aspose.words.net.system.data/datarelation/) utilizzando il nome specificato, le tabelle genitore e figlio, e gli array corrispondenti di colonne genitore e figlio. |
| [DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---boolean) | Inizializza una nuova istanza della classe [DataRelation](../../com.aspose.words.net.system.data/datarelation/) utilizzando il nome specificato, gli array corrispondenti di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) genitore e figlio, e il valore che indica se creare i vincoli. |
| [DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean) | Inizializza una nuova istanza della classe [DataRelation](../../com.aspose.words.net.system.data/datarelation/) utilizzando il nome specificato, gli oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) genitore e figlio, e un valore che indica se creare i vincoli. |
| [DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Inizializza una nuova istanza della classe [DataRelation](../../com.aspose.words.net.system.data/datarelation/) utilizzando il nome [DataRelation](../../com.aspose.words.net.system.data/datarelation/) specificato, e gli oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) genitore e figlio. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) |  |
| [getChildColumnNames()](#getChildColumnNames) |  |
| [getChildColumns()](#getChildColumns) | Restituisce gli oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) figlio di questa relazione. |
| [getChildKey()](#getChildKey) |  |
| [getChildKeyConstraint()](#getChildKeyConstraint) | Restituisce il [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) per la relazione. |
| [getChildTable()](#getChildTable) | Restituisce la tabella figlio di questa relazione. |
| [getChildTableName()](#getChildTableName) |  |
| [getDataSet()](#getDataSet) | Restituisce il [DataSet](../../com.aspose.words.net.system.data/dataset/) a cui appartiene il [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getParentColumnNames()](#getParentColumnNames) |  |
| [getParentColumns()](#getParentColumns) | Restituisce un array di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) che sono le colonne genitore di questo [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getParentKey()](#getParentKey) |  |
| [getParentKeyConstraint()](#getParentKeyConstraint) | Restituisce il [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) che garantisce che i valori nella colonna genitore di un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) siano unici. |
| [getParentTable()](#getParentTable) | Restituisce il [DataTable](../../com.aspose.words.net.system.data/datatable/) genitore di questo [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getParentTableName()](#getParentTableName) |  |
| [getRelationName()](#getRelationName) | Restituisce il nome usato per recuperare un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) dalla [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| [hashCode()](#hashCode) |  |
| [setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint)](#setChildKeyConstraint-com.aspose.words.net.System.Data.ForeignKeyConstraint) |  |
| [setNested(boolean value)](#setNested-boolean) | Imposta un valore che indica se gli oggetti [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sono nidificati. |
| [setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint)](#setParentKeyConstraint-com.aspose.words.net.System.Data.UniqueConstraint) |  |
### DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String}
```
public DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)
```


Inizializza una nuova istanza della classe [DataRelation](../../com.aspose.words.net.system.data/datarelation/) utilizzando il nome specificato, le tabelle genitore e figlio, e gli array corrispondenti di colonne genitore e figlio.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| relationName | java.lang.String | Il nome del DataRelation. Se null o una stringa vuota (""), verrà assegnato un nome predefinito quando l'oggetto creato viene aggiunto alla DataRelationCollection. |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | La tabella genitore nella relazione. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | La tabella figlia nella relazione. |
| parentColumnNames | java.lang.String[] | Il nome della DataColumn padre nella relazione. |
| childColumnNames | java.lang.String[] | Le DataColumn figlie nella relazione. |

### DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---boolean}
```
public DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints)
```


Inizializza una nuova istanza della classe [DataRelation](../../com.aspose.words.net.system.data/datarelation/) utilizzando il nome specificato, gli array corrispondenti di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) genitore e figlio, e il valore che indica se creare i vincoli.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| relationName | java.lang.String | Il nome della relazione. Se null o una stringa vuota (""), verrà assegnato un nome predefinito quando l'oggetto creato viene aggiunto al [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| parentColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Un array di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) genitore. |
| childColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Un array di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) figlio. |
| createConstraints | boolean | Un valore che indica se creare i vincoli. true, se i vincoli sono creati. Altrimenti, false. |

### DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean}
```
public DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)
```


Inizializza una nuova istanza della classe [DataRelation](../../com.aspose.words.net.system.data/datarelation/) utilizzando il nome specificato, gli oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) genitore e figlio, e un valore che indica se creare i vincoli.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| relationName | java.lang.String | Il nome della relazione. Se null o una stringa vuota (""), verrà assegnato un nome predefinito quando l'oggetto creato viene aggiunto al [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) genitore nella relazione. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) figlio nella relazione. |
| createConstraints | boolean | Un valore che indica se i vincoli sono creati. true, se i vincoli sono creati. Altrimenti, false. |

### DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Inizializza una nuova istanza della classe [DataRelation](../../com.aspose.words.net.system.data/datarelation/) utilizzando il nome [DataRelation](../../com.aspose.words.net.system.data/datarelation/) specificato, e gli oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) genitore e figlio.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| relationName | java.lang.String | Il nome del [DataRelation](../../com.aspose.words.net.system.data/datarelation/). Se null o una stringa vuota (""), verrà assegnato un nome predefinito quando l'oggetto creato viene aggiunto al [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) genitore nella relazione. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) figlio nella relazione. |

### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getChildColumnNames() {#getChildColumnNames}
```
public String[] getChildColumnNames()
```




**Returns:**
java.lang.String[] - i nomi delle DataColumn figlie di questa relazione.
### getChildColumns() {#getChildColumns}
```
public System.Data.DataColumn[] getChildColumns()
```


Restituisce gli oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) figlio di questa relazione.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Un array di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
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


Restituisce il [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) per la relazione.

**Returns:**
[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) - A [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/).
### getChildTable() {#getChildTable}
```
public System.Data.DataTable getChildTable()
```


Restituisce la tabella figlio di questa relazione.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the child table of the relation.
### getChildTableName() {#getChildTableName}
```
public String getChildTableName()
```




**Returns:**
java.lang.String - il nome della DataTable figlia di questo DataRelation.
### getDataSet() {#getDataSet}
```
public System.Data.DataSet getDataSet()
```


Restituisce il [DataSet](../../com.aspose.words.net.system.data/dataset/) a cui appartiene il [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Returns:**
[DataSet](../../com.aspose.words.net.system.data/dataset/) - A [DataSet](../../com.aspose.words.net.system.data/dataset/) to which the [DataRelation](../../com.aspose.words.net.system.data/datarelation/) belongs.
### getParentColumnNames() {#getParentColumnNames}
```
public String[] getParentColumnNames()
```




**Returns:**
java.lang.String[] - i nomi delle DataColumn genitore di questa relazione.
### getParentColumns() {#getParentColumns}
```
public System.Data.DataColumn[] getParentColumns()
```


Restituisce un array di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) che sono le colonne genitore di questo [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Un array di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) che sono le colonne genitore di questo [DataRelation](../../com.aspose.words.net.system.data/datarelation/).
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


Restituisce il [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) che garantisce che i valori nella colonna genitore di un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) siano unici.

**Returns:**
[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) - A [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) that makes sure that values in a parent column are unique.
### getParentTable() {#getParentTable}
```
public System.Data.DataTable getParentTable()
```


Restituisce il [DataTable](../../com.aspose.words.net.system.data/datatable/) genitore di questo [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the parent table of this relation.
### getParentTableName() {#getParentTableName}
```
public String getParentTableName()
```




**Returns:**
java.lang.String - il nome della DataTable genitore di questo DataRelation.
### getRelationName() {#getRelationName}
```
public String getRelationName()
```


Restituisce il nome usato per recuperare un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) dalla [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/).

**Returns:**
java.lang.String - Il nome di un [DataRelation](../../com.aspose.words.net.system.data/datarelation/).
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| childKeyConstraint | [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) |  |

### setNested(boolean value) {#setNested-boolean}
```
public void setNested(boolean value)
```


Imposta un valore che indica se gli oggetti [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sono nidificati.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | boolean | true, se gli oggetti [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sono nidificati; altrimenti, false. |

### setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint) {#setParentKeyConstraint-com.aspose.words.net.System.Data.UniqueConstraint}
```
public void setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| parentKeyConstraint | [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) |  |

