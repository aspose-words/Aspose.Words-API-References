---
title: "IDataReader"
linktitle: "IDataReader"
second_title: "Aspose.Words per Java"
description: "Fornisce un modo per leggere uno o più flussi forward-only di set di risultati ottenuti eseguendo un comando su una fonte dati ed è implementato dai provider di dati del .NET Framework che accedono a database relazionali in Java."
type: docs
weight: 34
url: /it/java/com.aspose.words.net.system.data/idatareader/
---

**All Implemented Interfaces:**
[com.aspose.words.net.System.Data.IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
```
public interface IDataReader extends System.Data.IDataRecord
```

Fornisce un modo per leggere uno o più flussi forward-only di set di risultati ottenuti eseguendo un comando su una fonte dati, ed è implementato dai provider di dati .NET Framework che accedono a database relazionali.
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [close()](#close) | Chiude l'oggetto [IDataReader](../../com.aspose.words.net.system.data/idatareader/). |
| [getDepth()](#getDepth) | Restituisce un valore che indica la profondità di nidificazione per la riga corrente. |
| [getRecordsAffected()](#getRecordsAffected) | Restituisce il numero di righe modificate, inserite o eliminate dall'esecuzione dell'istruzione SQL. |
| [getSchemaTable()](#getSchemaTable) | Restituisce un [DataTable](../../com.aspose.words.net.system.data/datatable/) che descrive i metadati delle colonne del [IDataReader](../../com.aspose.words.net.system.data/idatareader/). |
| [isClosed()](#isClosed) | Restituisce un valore che indica se il data reader è chiuso. |
| [nextResult()](#nextResult) | Avanza il data reader al risultato successivo, durante la lettura dei risultati di istruzioni SQL batch. |
| [read()](#read) | Avanza il [IDataReader](../../com.aspose.words.net.system.data/idatareader/) al record successivo. |
### close() {#close}
```
public abstract void close()
```


Chiude l'oggetto [IDataReader](../../com.aspose.words.net.system.data/idatareader/).

### getDepth() {#getDepth}
```
public abstract int getDepth()
```


Restituisce un valore che indica la profondità di nidificazione per la riga corrente.

**Returns:**
int - Il livello di nidificazione.
### getRecordsAffected() {#getRecordsAffected}
```
public abstract int getRecordsAffected()
```


Restituisce il numero di righe modificate, inserite o eliminate dall'esecuzione dell'istruzione SQL.

**Returns:**
int - Il numero di righe modificate, inserite o eliminate; 0 se nessuna riga è stata interessata o l'istruzione è fallita; e -1 per le istruzioni SELECT.
### getSchemaTable() {#getSchemaTable}
```
public abstract System.Data.DataTable getSchemaTable()
```


Restituisce un [DataTable](../../com.aspose.words.net.system.data/datatable/) che descrive i metadati delle colonne del [IDataReader](../../com.aspose.words.net.system.data/idatareader/).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that describes the column metadata.
### isClosed() {#isClosed}
```
public abstract boolean isClosed()
```


Restituisce un valore che indica se il data reader è chiuso.

**Returns:**
boolean - true se il data reader è chiuso; altrimenti, false.
### nextResult() {#nextResult}
```
public abstract boolean nextResult()
```


Avanza il data reader al risultato successivo, durante la lettura dei risultati di istruzioni SQL batch.

**Returns:**
boolean - true se ci sono altre righe; altrimenti, false.
### read() {#read}
```
public abstract boolean read()
```


Avanza il [IDataReader](../../com.aspose.words.net.system.data/idatareader/) al record successivo.

**Returns:**
boolean - true se ci sono altre righe; altrimenti, false.
