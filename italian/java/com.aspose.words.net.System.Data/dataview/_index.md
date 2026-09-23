---
title: "DataView"
linktitle: "DataView"
second_title: "Aspose.Words per Java"
description: "Rappresenta una vista personalizzata collegabile a dati di una DataTable per ordinamento, filtraggio, ricerca, modifica e navigazione in Java."
type: docs
weight: 28
url: /it/java/com.aspose.words.net.system.data/dataview/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataView implements Iterable
```

Rappresenta una vista personalizzata, collegabile a dati, di una [DataTable](../../com.aspose.words.net.system.data/datatable/) per ordinamento, filtraggio, ricerca, modifica e navigazione.
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [DataView(System.Data.DataTable table)](#DataView-com.aspose.words.net.System.Data.DataTable) | Inizializza una nuova istanza della classe [DataView](../../com.aspose.words.net.system.data/dataview/) con la [DataTable](../../com.aspose.words.net.system.data/datatable/) specificata. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [close()](#close) | Chiude la [DataView](../../com.aspose.words.net.system.data/dataview/). |
| [get(int recordIndex)](#get-int) | Ottiene una riga di dati da una tabella specificata. |
| [getCount()](#getCount) | Ottiene il numero di record nella [DataView](../../com.aspose.words.net.system.data/dataview/). |
| [getTable()](#getTable) | Ottiene la [DataTable](../../com.aspose.words.net.system.data/datatable/) di origine. |
| [iterator()](#iterator) | Ottiene un enumeratore per questa [DataView](../../com.aspose.words.net.system.data/dataview/). |
### DataView(System.Data.DataTable table) {#DataView-com.aspose.words.net.System.Data.DataTable}
```
public DataView(System.Data.DataTable table)
```


Inizializza una nuova istanza della classe [DataView](../../com.aspose.words.net.system.data/dataview/) con la [DataTable](../../com.aspose.words.net.system.data/datatable/) specificata.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Una [DataTable](../../com.aspose.words.net.system.data/datatable/) da aggiungere alla [DataView](../../com.aspose.words.net.system.data/dataview/). |

### close() {#close}
```
public void close()
```


Chiude la [DataView](../../com.aspose.words.net.system.data/dataview/).

### get(int recordIndex) {#get-int}
```
public System.Data.DataRowView get(int recordIndex)
```


Ottiene una riga di dati da una tabella specificata.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| recordIndex | int | L'indice di un record nella [DataTable](../../com.aspose.words.net.system.data/datatable/). |

**Returns:**
[DataRowView](../../com.aspose.words.net.system.data/datarowview/) - A [DataRowView](../../com.aspose.words.net.system.data/datarowview/) of the row that you want.
### getCount() {#getCount}
```
public int getCount()
```


Ottiene il numero di record nella [DataView](../../com.aspose.words.net.system.data/dataview/).

**Returns:**
int - Il numero di record nella [DataView](../../com.aspose.words.net.system.data/dataview/).
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Ottiene la [DataTable](../../com.aspose.words.net.system.data/datatable/) di origine.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that provides the data for this view.
### iterator() {#iterator}
```
public Iterator iterator()
```


Ottiene un enumeratore per questa [DataView](../../com.aspose.words.net.system.data/dataview/).

**Returns:**
java.util.Iterator - Un java.util.Iterator per navigare nell'elenco.
