---
title: "IDataReader"
linktitle: "IDataReader"
second_title: "Aspose.Words für Java"
description: "Stellt eine Möglichkeit zum Lesen von einem oder mehreren vorwärtsgerichteten Datenströmen von Ergebnissets bereit, die durch Ausführen eines Befehls an einer Datenquelle erhalten werden, und wird von .NET Framework-Datenanbietern implementiert, die in Java auf relationale Datenbanken zugreifen."
type: docs
weight: 34
url: /de/java/com.aspose.words.net.system.data/idatareader/
---

**All Implemented Interfaces:**
[com.aspose.words.net.System.Data.IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
```
public interface IDataReader extends System.Data.IDataRecord
```

Bietet eine Möglichkeit, einen oder mehrere vorwärtsgerichtete Streams von Ergebnissets zu lesen, die durch Ausführen eines Befehls an einer Datenquelle erhalten wurden, und wird von .NET Framework-Datenanbietern implementiert, die relationale Datenbanken zugreifen.
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [close()](#close) | Schließt das [IDataReader](../../com.aspose.words.net.system.data/idatareader/) Objekt. |
| [getDepth()](#getDepth) | Gibt einen Wert zurück, der die Verschachtelungstiefe für die aktuelle Zeile angibt. |
| [getRecordsAffected()](#getRecordsAffected) | Gibt die Anzahl der durch die Ausführung der SQL-Anweisung geänderten, eingefügten oder gelöschten Zeilen zurück. |
| [getSchemaTable()](#getSchemaTable) | Gibt eine [DataTable](../../com.aspose.words.net.system.data/datatable/) zurück, die die Spalten-Metadaten des [IDataReader](../../com.aspose.words.net.system.data/idatareader/) beschreibt. |
| [isClosed()](#isClosed) | Gibt einen Wert zurück, der angibt, ob der Datenleser geschlossen ist. |
| [nextResult()](#nextResult) | Führt den Datenleser zum nächsten Ergebnis, wenn die Ergebnisse von Batch‑SQL‑Anweisungen gelesen werden. |
| [read()](#read) | Führt den [IDataReader](../../com.aspose.words.net.system.data/idatareader/) zum nächsten Datensatz. |
### close() {#close}
```
public abstract void close()
```


Schließt das [IDataReader](../../com.aspose.words.net.system.data/idatareader/) Objekt.

### getDepth() {#getDepth}
```
public abstract int getDepth()
```


Gibt einen Wert zurück, der die Verschachtelungstiefe für die aktuelle Zeile angibt.

**Returns:**
int – Die Verschachtelungsebene.
### getRecordsAffected() {#getRecordsAffected}
```
public abstract int getRecordsAffected()
```


Gibt die Anzahl der durch die Ausführung der SQL-Anweisung geänderten, eingefügten oder gelöschten Zeilen zurück.

**Returns:**
int – Die Anzahl der geänderten, eingefügten oder gelöschten Zeilen; 0, wenn keine Zeilen betroffen waren oder die Anweisung fehlgeschlagen ist; und -1 für SELECT‑Anweisungen.
### getSchemaTable() {#getSchemaTable}
```
public abstract System.Data.DataTable getSchemaTable()
```


Gibt eine [DataTable](../../com.aspose.words.net.system.data/datatable/) zurück, die die Spalten-Metadaten des [IDataReader](../../com.aspose.words.net.system.data/idatareader/) beschreibt.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that describes the column metadata.
### isClosed() {#isClosed}
```
public abstract boolean isClosed()
```


Gibt einen Wert zurück, der angibt, ob der Datenleser geschlossen ist.

**Returns:**
boolean – true, wenn der Datenleser geschlossen ist; andernfalls false.
### nextResult() {#nextResult}
```
public abstract boolean nextResult()
```


Führt den Datenleser zum nächsten Ergebnis, wenn die Ergebnisse von Batch‑SQL‑Anweisungen gelesen werden.

**Returns:**
boolean – true, wenn weitere Zeilen vorhanden sind; andernfalls false.
### read() {#read}
```
public abstract boolean read()
```


Führt den [IDataReader](../../com.aspose.words.net.system.data/idatareader/) zum nächsten Datensatz.

**Returns:**
boolean – true, wenn weitere Zeilen vorhanden sind; andernfalls false.
