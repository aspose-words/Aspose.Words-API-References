---
title: "DataTable"
linktitle: "DataTable"
second_title: "Aspose.Words per Java"
description: "Rappresenta una tabella di dati in memoria in Java."
type: docs
weight: 25
url: /it/java/com.aspose.words.net.system.data/datatable/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.net.System.Data.DataTableEventListener](../../com.aspose.words.net.system.data/datatableeventlistener/)
```
public class DataTable implements System.Data.DataTableEventListener
```

Rappresenta una tabella di dati in memoria.
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [DataTable()](#DataTable) | Inizializza una nuova istanza della classe [DataTable](../../com.aspose.words.net.system.data/datatable/) senza argomenti. |
| [DataTable(String tableName)](#DataTable-java.lang.String) | Inizializza una nuova istanza della classe [DataTable](../../com.aspose.words.net.system.data/datatable/) con il nome della tabella specificato. |
| [DataTable(ResultSet resultSet)](#DataTable-java.sql.ResultSet) | Crea un oggetto avvolgendo il ResultSet specificato. |
| [DataTable(ResultSet resultSet, String tableName)](#DataTable-java.sql.ResultSet-java.lang.String) | Crea un oggetto avvolgendo il ResultSet specificato. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [acceptChanges()](#acceptChanges) | Conferma tutte le modifiche apportate a questa tabella dall'ultima volta che è stato chiamato [acceptChanges()](../../com.aspose.words.net.system.data/datatable/\#acceptChanges). |
| [addEventListener(System.Data.DataTableEventListener listener)](#addEventListener-com.aspose.words.net.System.Data.DataTableEventListener) |  |
| [clearEventListneers()](#clearEventListneers) |  |
| [close()](#close) |  |
| [containsColumn(String columnName)](#containsColumn-java.lang.String) | Verifica se la colonna fornita esiste o meno |
| [getChildRelations()](#getChildRelations) | Ottiene la raccolta delle relazioni figlie per questo [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getColumnName(int index)](#getColumnName-int) | Analogo per .Net DataTable.Columns[i].ColumnName |
| [getColumns()](#getColumns) | Ottiene la raccolta delle colonne che appartengono a questa tabella. |
| [getColumnsCount()](#getColumnsCount) |  |
| [getConstraints()](#getConstraints) | Ottiene la raccolta dei vincoli mantenuti da questa tabella. |
| [getDataSet()](#getDataSet) | Ottiene il [DataSet](../../com.aspose.words.net.system.data/dataset/) a cui appartiene questa tabella. |
| [getEnforceConstraints()](#getEnforceConstraints) |  |
| [getNamespace()](#getNamespace) | Ottiene lo spazio dei nomi per la rappresentazione XML dei dati memorizzati nel [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getParentRelations()](#getParentRelations) | Ottiene la raccolta delle relazioni genitore per questo [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getPrimaryKey()](#getPrimaryKey) | Ottiene un array di colonne che fungono da chiavi primarie per la tabella dati. |
| [getResultSet()](#getResultSet) | Restituisce l'oggetto Java ResultSet sottostante. |
| [getRows()](#getRows) | Ottiene la raccolta delle righe che appartengono a questa tabella. |
| [getTableName()](#getTableName) | Ottiene il nome del [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [newRow()](#newRow) | Crea un nuovo [DataRow](../../com.aspose.words.net.system.data/datarow/) con lo stesso schema della tabella. |
| [onDataColumnDeleted(System.Data.DataColumn column)](#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn) |  |
| [onDataColumnInserted(System.Data.DataColumn column)](#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn) |  |
| [onDataRowChanged(System.Data.DataRow row)](#onDataRowChanged-com.aspose.words.net.System.Data.DataRow) |  |
| [onDataRowDeleted(System.Data.DataRow row)](#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow) |  |
| [onDataRowInserted(System.Data.DataRow row)](#onDataRowInserted-com.aspose.words.net.System.Data.DataRow) |  |
| [refresh()](#refresh) | Ricarica tutti i dati dal ResultSet se è presente. |
| [setEnforceConstraints(boolean enforceConstraints)](#setEnforceConstraints-boolean) |  |
| [setNamespace(String value)](#setNamespace-java.lang.String) | Imposta lo spazio dei nomi per la rappresentazione XML dei dati memorizzati nel [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [setPrimaryKey(System.Data.DataColumn[] value)](#setPrimaryKey-com.aspose.words.net.System.Data.DataColumn) | Imposta un array di colonne che fungono da chiavi primarie per la tabella dati. |
| [setTableName(String value)](#setTableName-java.lang.String) | Imposta il nome del [DataTable](../../com.aspose.words.net.system.data/datatable/). |
### DataTable() {#DataTable}
```
public DataTable()
```


Inizializza una nuova istanza della classe [DataTable](../../com.aspose.words.net.system.data/datatable/) senza argomenti.

### DataTable(String tableName) {#DataTable-java.lang.String}
```
public DataTable(String tableName)
```


Inizializza una nuova istanza della classe [DataTable](../../com.aspose.words.net.system.data/datatable/) con il nome della tabella specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableName | java.lang.String | Il nome da assegnare alla tabella. Se  tableName  è null o una stringa vuota, viene assegnato un nome predefinito quando viene aggiunto al [DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/). |

### DataTable(ResultSet resultSet) {#DataTable-java.sql.ResultSet}
```
public DataTable(ResultSet resultSet)
```


Crea un oggetto avvolgendo il ResultSet specificato. Tenta di recuperare il nome della tabella dai metadati della prima colonna del ResultSet.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | set di dati |

### DataTable(ResultSet resultSet, String tableName) {#DataTable-java.sql.ResultSet-java.lang.String}
```
public DataTable(ResultSet resultSet, String tableName)
```


Crea un oggetto avvolgendo il ResultSet specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | set di dati |
| tableName | java.lang.String | nome della tabella |

### acceptChanges() {#acceptChanges}
```
public void acceptChanges()
```


Conferma tutte le modifiche apportate a questa tabella dall'ultima volta che è stato chiamato [acceptChanges()](../../com.aspose.words.net.system.data/datatable/\#acceptChanges).

### addEventListener(System.Data.DataTableEventListener listener) {#addEventListener-com.aspose.words.net.System.Data.DataTableEventListener}
```
public synchronized void addEventListener(System.Data.DataTableEventListener listener)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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


Verifica se la colonna fornita esiste o meno

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| columnName | java.lang.String | nome della colonna |

**Returns:**
boolean - `true` indica che la colonna può essere trovata con il `columnName` fornito
### getChildRelations() {#getChildRelations}
```
public System.Data.DataRelationCollection getChildRelations()
```


Ottiene la raccolta delle relazioni figlie per questo [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains the child relations for the table. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getColumnName(int index) {#getColumnName-int}
```
public String getColumnName(int index)
```


Analogo per .Net DataTable.Columns[i].ColumnName

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | \- indice della colonna |

**Returns:**
java.lang.String - nome della colonna per il suo indice.
### getColumns() {#getColumns}
```
public System.Data.DataColumnCollection getColumns()
```


Ottiene la raccolta delle colonne che appartengono a questa tabella.

**Returns:**
[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) - A [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) that contains the collection of [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects for the table. An empty collection is returned if no [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects exist.
### getColumnsCount() {#getColumnsCount}
```
public int getColumnsCount()
```




**Returns:**
int - conteggio delle colonne
### getConstraints() {#getConstraints}
```
public System.Data.ConstraintCollection getConstraints()
```


Ottiene la raccolta dei vincoli mantenuti da questa tabella.

**Returns:**
[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) - A [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) that contains the collection of [Constraint](../../com.aspose.words.net.system.data/constraint/) objects for the table. An empty collection is returned if no [Constraint](../../com.aspose.words.net.system.data/constraint/) objects exist.
### getDataSet() {#getDataSet}
```
public System.Data.DataSet getDataSet()
```


Ottiene il [DataSet](../../com.aspose.words.net.system.data/dataset/) a cui appartiene questa tabella.

**Returns:**
[DataSet](../../com.aspose.words.net.system.data/dataset/) - The [DataSet](../../com.aspose.words.net.system.data/dataset/) to which this table belongs.
### getEnforceConstraints() {#getEnforceConstraints}
```
public boolean getEnforceConstraints()
```




**Returns:**
boolean - flag che indica se c'è una violazione del vincolo di controllo o meno
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


Ottiene lo spazio dei nomi per la rappresentazione XML dei dati memorizzati nel [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
java.lang.String - Lo spazio dei nomi del [DataTable](../../com.aspose.words.net.system.data/datatable/).
### getParentRelations() {#getParentRelations}
```
public System.Data.DataRelationCollection getParentRelations()
```


Ottiene la raccolta delle relazioni genitore per questo [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains the parent relations for the table. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getPrimaryKey() {#getPrimaryKey}
```
public System.Data.DataColumn[] getPrimaryKey()
```


Ottiene un array di colonne che fungono da chiavi primarie per la tabella dati.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Un array di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getResultSet() {#getResultSet}
```
public ResultSet getResultSet()
```


Restituisce l'oggetto Java ResultSet sottostante. Idealmente vorremmo lavorare con DataTable in modo .Net. Tuttavia alcuni utenti e persino alcuni dei nostri esempi di codice stanno usando questa proprietà.

**Returns:**
java.sql.ResultSet - il java.sql.ResultSet sottostante
### getRows() {#getRows}
```
public System.Data.DataRowCollection getRows()
```


Ottiene la raccolta delle righe che appartengono a questa tabella.

**Returns:**
[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) - A [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) that contains [DataRow](../../com.aspose.words.net.system.data/datarow/) objects; otherwise a null value if no [DataRow](../../com.aspose.words.net.system.data/datarow/) objects exist.
### getTableName() {#getTableName}
```
public String getTableName()
```


Ottiene il nome del [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
java.lang.String - Il nome del [DataTable](../../com.aspose.words.net.system.data/datatable/).
### newRow() {#newRow}
```
public System.Data.DataRow newRow()
```


Crea un nuovo [DataRow](../../com.aspose.words.net.system.data/datarow/) con lo stesso schema della tabella.

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A [DataRow](../../com.aspose.words.net.system.data/datarow/) with the same schema as the [DataTable](../../com.aspose.words.net.system.data/datatable/).
### onDataColumnDeleted(System.Data.DataColumn column) {#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn}
```
public void onDataColumnDeleted(System.Data.DataColumn column)
```


Aggiorna listener quando DataColumn eliminata

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) |  |

### onDataColumnInserted(System.Data.DataColumn column) {#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn}
```
public void onDataColumnInserted(System.Data.DataColumn column)
```


Aggiorna listener quando DataColumn inserita

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) |  |

### onDataRowChanged(System.Data.DataRow row) {#onDataRowChanged-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowChanged(System.Data.DataRow row)
```


Aggiorna listener quando DataRow modificata

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### onDataRowDeleted(System.Data.DataRow row) {#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowDeleted(System.Data.DataRow row)
```


Aggiorna listener quando DataRow eliminata

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### onDataRowInserted(System.Data.DataRow row) {#onDataRowInserted-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowInserted(System.Data.DataRow row)
```


Aggiorna listener quando DataRow inserito

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### refresh() {#refresh}
```
public void refresh()
```


Ricarica tutti i dati dal ResultSet se è presente.

### setEnforceConstraints(boolean enforceConstraints) {#setEnforceConstraints-boolean}
```
public void setEnforceConstraints(boolean enforceConstraints)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| enforceConstraints | boolean | è il flag che indica se c'è una violazione del vincolo di controllo o meno |

### setNamespace(String value) {#setNamespace-java.lang.String}
```
public void setNamespace(String value)
```


Imposta lo spazio dei nomi per la rappresentazione XML dei dati memorizzati nel [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | java.lang.String | Lo spazio dei nomi del [DataTable](../../com.aspose.words.net.system.data/datatable/). |

### setPrimaryKey(System.Data.DataColumn[] value) {#setPrimaryKey-com.aspose.words.net.System.Data.DataColumn}
```
public void setPrimaryKey(System.Data.DataColumn[] value)
```


Imposta un array di colonne che fungono da chiavi primarie per la tabella dati.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Un array di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |

### setTableName(String value) {#setTableName-java.lang.String}
```
public void setTableName(String value)
```


Imposta il nome del [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | java.lang.String | Il nome del [DataTable](../../com.aspose.words.net.system.data/datatable/). |

