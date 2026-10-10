---
title: "DataTableReader"
linktitle: "DataTableReader"
second_title: "Aspose.Words per Java"
description: "Il DataTableReader ottiene il contenuto di uno o più oggetti DataTable sotto forma di uno o più set di risultati di sola lettura, in avanti, in Java."
type: docs
weight: 27
url: /it/java/com.aspose.words.net.system.data/datatablereader/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Common.DbDataReader](../../com.aspose.words.net.system.data.common/dbdatareader/)
```
public class DataTableReader extends System.Data.Common.DbDataReader
```

Il [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) ottiene il contenuto di uno o più oggetti [DataTable](../../com.aspose.words.net.system.data/datatable/) sotto forma di uno o più set di risultati di sola lettura, in avanti.
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [DataTableReader(System.Data.DataTable dataTable)](#DataTableReader-com.aspose.words.net.System.Data.DataTable) | Inizializza una nuova istanza della classe [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) utilizzando i dati della [DataTable](../../com.aspose.words.net.system.data/datatable/) fornita. |
| [DataTableReader(System.Data.DataTable[] dataTables)](#DataTableReader-com.aspose.words.net.System.Data.DataTable) | Inizializza una nuova istanza della classe [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) utilizzando l'array fornito di oggetti [DataTable](../../com.aspose.words.net.system.data/datatable/). |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [close()](#close) | Chiude l'attuale [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/). |
| [get(int ordinal)](#get-int) | Restituisce il valore della colonna specificata nel suo formato nativo dato l'indice della colonna. |
| [get(String name)](#get-java.lang.String) | Restituisce il valore della colonna specificata nel suo formato nativo dato il nome della colonna. |
| [getDepth()](#getDepth) | La profondità di annidamento per la riga corrente del [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/). |
| [getFieldCount()](#getFieldCount) | Restituisce il numero di colonne nella riga corrente. |
| [getFieldType(int ordinal)](#getFieldType-int) | Restituisce il java.lang.Class che è il tipo di dato dell'oggetto. |
| [getName(int ordinal)](#getName-int) | Restituisce il valore della colonna specificata come java.lang.String. |
| [getRecordsAffected()](#getRecordsAffected) | Restituisce il numero di righe inserite, modificate o eliminate dall'esecuzione dell'istruzione SQL. |
| [getSchemaTable()](#getSchemaTable) | Restituisce un [DataTable](../../com.aspose.words.net.system.data/datatable/) che descrive i metadati delle colonne del [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/). |
| [getValue(int ordinal)](#getValue-int) | Restituisce il valore della colonna specificata nel suo formato nativo. |
| [hasRows()](#hasRows) | Restituisce un valore che indica se il [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) contiene una o più righe. |
| [isClosed()](#isClosed) | Restituisce un valore che indica se il [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) è chiuso. |
| [iterator()](#iterator) | Restituisce un enumeratore che può essere usato per iterare attraverso la collezione di elementi. |
| [nextResult()](#nextResult) | Avanza il [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) al prossimo set di risultati, se presente. |
| [read()](#read) | Avanza il [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) al record successivo. |
### DataTableReader(System.Data.DataTable dataTable) {#DataTableReader-com.aspose.words.net.System.Data.DataTable}
```
public DataTableReader(System.Data.DataTable dataTable)
```


Inizializza una nuova istanza della classe [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) utilizzando i dati della [DataTable](../../com.aspose.words.net.system.data/datatable/) fornita.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Il [DataTable](../../com.aspose.words.net.system.data/datatable/) da cui il nuovo [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) ottiene il suo set di risultati. |

### DataTableReader(System.Data.DataTable[] dataTables) {#DataTableReader-com.aspose.words.net.System.Data.DataTable}
```
public DataTableReader(System.Data.DataTable[] dataTables)
```


Inizializza una nuova istanza della classe [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) utilizzando l'array fornito di oggetti [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataTables | [DataTable\[\]](../../com.aspose.words.net.system.data/datatable/) | L'array di oggetti [DataTable](../../com.aspose.words.net.system.data/datatable/) che fornisce i risultati per il nuovo oggetto [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/). |

### close() {#close}
```
public void close()
```


Chiude l'attuale [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/).

### get(int ordinal) {#get-int}
```
public Object get(int ordinal)
```


Restituisce il valore della colonna specificata nel suo formato nativo dato l'indice della colonna.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice della colonna basato su zero. |

**Returns:**
java.lang.Object - Il valore della colonna specificata nel suo formato nativo.
### get(String name) {#get-java.lang.String}
```
public Object get(String name)
```


Restituisce il valore della colonna specificata nel suo formato nativo dato il nome della colonna.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome della colonna. |

**Returns:**
java.lang.Object - Il valore della colonna specificata nel suo formato nativo.
### getDepth() {#getDepth}
```
public int getDepth()
```


La profondità di annidamento per la riga corrente del [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/).

**Returns:**
int - La profondità di annidamento per la riga corrente; sempre zero.
### getFieldCount() {#getFieldCount}
```
public int getFieldCount()
```


Restituisce il numero di colonne nella riga corrente.

**Returns:**
int - Quando non è posizionato in un set di risultati valido, 0; altrimenti il numero di colonne nella riga corrente.
### getFieldType(int ordinal) {#getFieldType-int}
```
public Class getFieldType(int ordinal)
```


Restituisce il java.lang.Class che è il tipo di dato dell'oggetto.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice della colonna basato su zero. |

**Returns:**
java.lang.Class - Il java.lang.Class che è il tipo di dato dell'oggetto.
### getName(int ordinal) {#getName-int}
```
public String getName(int ordinal)
```


Restituisce il valore della colonna specificata come java.lang.String.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice della colonna basato su zero |

**Returns:**
java.lang.String - Il nome della colonna specificata.
### getRecordsAffected() {#getRecordsAffected}
```
public int getRecordsAffected()
```


Restituisce il numero di righe inserite, modificate o eliminate dall'esecuzione dell'istruzione SQL.

**Returns:**
int - Il [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) non supporta questa proprietà e restituisce sempre 0.
### getSchemaTable() {#getSchemaTable}
```
public System.Data.DataTable getSchemaTable()
```


Restituisce un [DataTable](../../com.aspose.words.net.system.data/datatable/) che descrive i metadati delle colonne del [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that describes the column metadata.
### getValue(int ordinal) {#getValue-int}
```
public Object getValue(int ordinal)
```


Restituisce il valore della colonna specificata nel suo formato nativo.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice della colonna basato su zero |

**Returns:**
java.lang.Object - Il valore della colonna specificata. Questo metodo restituisce DBNull per le colonne nulle.
### hasRows() {#hasRows}
```
public boolean hasRows()
```


Restituisce un valore che indica se il [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) contiene una o più righe.

**Returns:**
boolean - true se il [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) contiene una o più righe; altrimenti false.
### isClosed() {#isClosed}
```
public boolean isClosed()
```


Restituisce un valore che indica se il [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) è chiuso.

**Returns:**
boolean - Restituisce true se il [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) è chiuso; altrimenti false.
### iterator() {#iterator}
```
public Iterator iterator()
```


Restituisce un enumeratore che può essere usato per iterare attraverso la collezione di elementi.

**Returns:**
java.util.Iterator - Un oggetto java.util.Iterator che rappresenta la collezione di elementi.
### nextResult() {#nextResult}
```
public boolean nextResult()
```


Avanza il [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) al prossimo set di risultati, se presente.

**Returns:**
boolean - true se c'era un altro set di risultati; altrimenti false.
### read() {#read}
```
public boolean read()
```


Avanza il [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) al record successivo.

**Returns:**
boolean - true se c'era un'altra riga da leggere; altrimenti false.
