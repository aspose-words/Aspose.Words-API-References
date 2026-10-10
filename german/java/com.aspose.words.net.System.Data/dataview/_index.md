---
title: "DataView"
linktitle: "DataView"
second_title: "Aspose.Words für Java"
description: "Stellt eine databindbare, angepasste Ansicht einer DataTable für Sortieren, Filtern, Suchen, Bearbeiten und Navigation in Java dar."
type: docs
weight: 28
url: /de/java/com.aspose.words.net.system.data/dataview/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataView implements Iterable
```

Stellt eine databindbare, angepasste Ansicht einer [DataTable](../../com.aspose.words.net.system.data/datatable/) für Sortieren, Filtern, Suchen, Bearbeiten und Navigation dar.
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [DataView(System.Data.DataTable table)](#DataView-com.aspose.words.net.System.Data.DataTable) | Initialisiert eine neue Instanz der Klasse [DataView](../../com.aspose.words.net.system.data/dataview/) mit der angegebenen [DataTable](../../com.aspose.words.net.system.data/datatable/). |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [close()](#close) | Schließt die [DataView](../../com.aspose.words.net.system.data/dataview/). |
| [get(int recordIndex)](#get-int) | Ruft eine Datenzeile aus einer angegebenen Tabelle ab. |
| [getCount()](#getCount) | Ruft die Anzahl der Datensätze in der [DataView](../../com.aspose.words.net.system.data/dataview/) ab. |
| [getTable()](#getTable) | Ruft die Quell-[DataTable](../../com.aspose.words.net.system.data/datatable/) ab. |
| [iterator()](#iterator) | Ruft einen Enumerator für diese [DataView](../../com.aspose.words.net.system.data/dataview/) ab. |
### DataView(System.Data.DataTable table) {#DataView-com.aspose.words.net.System.Data.DataTable}
```
public DataView(System.Data.DataTable table)
```


Initialisiert eine neue Instanz der Klasse [DataView](../../com.aspose.words.net.system.data/dataview/) mit der angegebenen [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Eine [DataTable](../../com.aspose.words.net.system.data/datatable/) zum Hinzufügen zur [DataView](../../com.aspose.words.net.system.data/dataview/). |

### close() {#close}
```
public void close()
```


Schließt die [DataView](../../com.aspose.words.net.system.data/dataview/).

### get(int recordIndex) {#get-int}
```
public System.Data.DataRowView get(int recordIndex)
```


Ruft eine Datenzeile aus einer angegebenen Tabelle ab.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| recordIndex | int | Der Index eines Datensatzes in der [DataTable](../../com.aspose.words.net.system.data/datatable/). |

**Returns:**
[DataRowView](../../com.aspose.words.net.system.data/datarowview/) - A [DataRowView](../../com.aspose.words.net.system.data/datarowview/) of the row that you want.
### getCount() {#getCount}
```
public int getCount()
```


Ruft die Anzahl der Datensätze in der [DataView](../../com.aspose.words.net.system.data/dataview/) ab.

**Returns:**
int - Die Anzahl der Datensätze in der [DataView](../../com.aspose.words.net.system.data/dataview/).
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Ruft die Quell-[DataTable](../../com.aspose.words.net.system.data/datatable/) ab.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that provides the data for this view.
### iterator() {#iterator}
```
public Iterator iterator()
```


Ruft einen Enumerator für diese [DataView](../../com.aspose.words.net.system.data/dataview/) ab.

**Returns:**
java.util.Iterator - Ein java.util.Iterator zum Durchlaufen der Liste.
