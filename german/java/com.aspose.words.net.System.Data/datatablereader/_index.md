---
title: "DataTableReader"
linktitle: "DataTableReader"
second_title: "Aspose.Words für Java"
description: "Der DataTableReader ruft den Inhalt von einem oder mehreren DataTable-Objekten in Form von einem oder mehreren schreibgeschützten, vorwärtsgerichteten Resultatsets in Java ab."
type: docs
weight: 27
url: /de/java/com.aspose.words.net.system.data/datatablereader/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Common.DbDataReader](../../com.aspose.words.net.system.data.common/dbdatareader/)
```
public class DataTableReader extends System.Data.Common.DbDataReader
```

Der [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) ruft den Inhalt von einem oder mehreren [DataTable](../../com.aspose.words.net.system.data/datatable/) Objekten in Form von einem oder mehreren schreibgeschützten, vorwärtsgerichteten Resultatsets ab.
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [DataTableReader(System.Data.DataTable dataTable)](#DataTableReader-com.aspose.words.net.System.Data.DataTable) | Initialisiert eine neue Instanz der Klasse [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) indem Daten aus dem bereitgestellten [DataTable](../../com.aspose.words.net.system.data/datatable/) verwendet werden. |
| [DataTableReader(System.Data.DataTable[] dataTables)](#DataTableReader-com.aspose.words.net.System.Data.DataTable) | Initialisiert eine neue Instanz der Klasse [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/), indem das bereitgestellte Array von [DataTable](../../com.aspose.words.net.system.data/datatable/)-Objekten verwendet wird. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [close()](#close) | Schließt den aktuellen [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/). |
| [get(int ordinal)](#get-int) | Gibt den Wert der angegebenen Spalte in ihrem nativen Format zurück, basierend auf dem Spaltenordinal. |
| [get(String name)](#get-java.lang.String) | Gibt den Wert der angegebenen Spalte in ihrem nativen Format zurück, basierend auf dem Spaltennamen. |
| [getDepth()](#getDepth) | Die Verschachtelungstiefe für die aktuelle Zeile des [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/). |
| [getFieldCount()](#getFieldCount) | Gibt die Anzahl der Spalten in der aktuellen Zeile zurück. |
| [getFieldType(int ordinal)](#getFieldType-int) | Gibt die java.lang.Class zurück, die den Datentyp des Objekts darstellt. |
| [getName(int ordinal)](#getName-int) | Gibt den Wert der angegebenen Spalte als java.lang.String zurück. |
| [getRecordsAffected()](#getRecordsAffected) | Gibt die Anzahl der durch die Ausführung der SQL-Anweisung eingefügten, geänderten oder gelöschten Zeilen zurück. |
| [getSchemaTable()](#getSchemaTable) | Gibt ein [DataTable](../../com.aspose.words.net.system.data/datatable/) zurück, das die Spaltenmetadaten des [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) beschreibt. |
| [getValue(int ordinal)](#getValue-int) | Gibt den Wert der angegebenen Spalte in ihrem nativen Format zurück. |
| [hasRows()](#hasRows) | Gibt einen Wert zurück, der angibt, ob der [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) eine oder mehrere Zeilen enthält. |
| [isClosed()](#isClosed) | Gibt einen Wert zurück, der angibt, ob der [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) geschlossen ist. |
| [iterator()](#iterator) | Gibt einen Enumerator zurück, der verwendet werden kann, um durch die Elementsammlung zu iterieren. |
| [nextResult()](#nextResult) | Bewegt den [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) zum nächsten Resultatset, falls vorhanden. |
| [read()](#read) | Bewegt den [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) zum nächsten Datensatz. |
### DataTableReader(System.Data.DataTable dataTable) {#DataTableReader-com.aspose.words.net.System.Data.DataTable}
```
public DataTableReader(System.Data.DataTable dataTable)
```


Initialisiert eine neue Instanz der Klasse [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) indem Daten aus dem bereitgestellten [DataTable](../../com.aspose.words.net.system.data/datatable/) verwendet werden.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Das [DataTable](../../com.aspose.words.net.system.data/datatable/), aus dem der neue [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) sein Resultatset bezieht. |

### DataTableReader(System.Data.DataTable[] dataTables) {#DataTableReader-com.aspose.words.net.System.Data.DataTable}
```
public DataTableReader(System.Data.DataTable[] dataTables)
```


Initialisiert eine neue Instanz der Klasse [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/), indem das bereitgestellte Array von [DataTable](../../com.aspose.words.net.system.data/datatable/)-Objekten verwendet wird.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataTables | [DataTable\[\]](../../com.aspose.words.net.system.data/datatable/) | Das Array von [DataTable](../../com.aspose.words.net.system.data/datatable/)-Objekten, das die Ergebnisse für das neue [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/)-Objekt bereitstellt. |

### close() {#close}
```
public void close()
```


Schließt den aktuellen [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/).

### get(int ordinal) {#get-int}
```
public Object get(int ordinal)
```


Gibt den Wert der angegebenen Spalte in ihrem nativen Format zurück, basierend auf dem Spaltenordinal.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ordinal | int | Der nullbasierte Spaltenordinal. |

**Returns:**
java.lang.Object - Der Wert der angegebenen Spalte in ihrem nativen Format.
### get(String name) {#get-java.lang.String}
```
public Object get(String name)
```


Gibt den Wert der angegebenen Spalte in ihrem nativen Format zurück, basierend auf dem Spaltennamen.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name der Spalte. |

**Returns:**
java.lang.Object - Der Wert der angegebenen Spalte in ihrem nativen Format.
### getDepth() {#getDepth}
```
public int getDepth()
```


Die Verschachtelungstiefe für die aktuelle Zeile des [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/).

**Returns:**
int - Die Verschachtelungstiefe für die aktuelle Zeile; immer null.
### getFieldCount() {#getFieldCount}
```
public int getFieldCount()
```


Gibt die Anzahl der Spalten in der aktuellen Zeile zurück.

**Returns:**
int - Wenn nicht in einem gültigen Ergebnis‑Set positioniert, 0; andernfalls die Anzahl der Spalten in der aktuellen Zeile.
### getFieldType(int ordinal) {#getFieldType-int}
```
public Class getFieldType(int ordinal)
```


Gibt die java.lang.Class zurück, die den Datentyp des Objekts darstellt.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ordinal | int | Der nullbasierte Spaltenordinal. |

**Returns:**
java.lang.Class - Die java.lang.Class, die den Datentyp des Objekts darstellt.
### getName(int ordinal) {#getName-int}
```
public String getName(int ordinal)
```


Gibt den Wert der angegebenen Spalte als java.lang.String zurück.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ordinal | int | Der nullbasierte Spaltenordinal |

**Returns:**
java.lang.String - Der Name der angegebenen Spalte.
### getRecordsAffected() {#getRecordsAffected}
```
public int getRecordsAffected()
```


Gibt die Anzahl der durch die Ausführung der SQL-Anweisung eingefügten, geänderten oder gelöschten Zeilen zurück.

**Returns:**
int - Der [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) unterstützt diese Eigenschaft nicht und gibt immer 0 zurück.
### getSchemaTable() {#getSchemaTable}
```
public System.Data.DataTable getSchemaTable()
```


Gibt ein [DataTable](../../com.aspose.words.net.system.data/datatable/) zurück, das die Spaltenmetadaten des [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) beschreibt.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that describes the column metadata.
### getValue(int ordinal) {#getValue-int}
```
public Object getValue(int ordinal)
```


Gibt den Wert der angegebenen Spalte in ihrem nativen Format zurück.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ordinal | int | Der nullbasierte Spaltenordinal |

**Returns:**
java.lang.Object - Der Wert der angegebenen Spalte. Diese Methode gibt DBNull für null‑Spalten zurück.
### hasRows() {#hasRows}
```
public boolean hasRows()
```


Gibt einen Wert zurück, der angibt, ob der [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) eine oder mehrere Zeilen enthält.

**Returns:**
boolean - true, wenn der [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) eine oder mehrere Zeilen enthält; andernfalls false.
### isClosed() {#isClosed}
```
public boolean isClosed()
```


Gibt einen Wert zurück, der angibt, ob der [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) geschlossen ist.

**Returns:**
boolean - Gibt true zurück, wenn der [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) geschlossen ist; andernfalls false.
### iterator() {#iterator}
```
public Iterator iterator()
```


Gibt einen Enumerator zurück, der verwendet werden kann, um durch die Elementsammlung zu iterieren.

**Returns:**
java.util.Iterator - Ein java.util.Iterator‑Objekt, das die Elementsammlung darstellt.
### nextResult() {#nextResult}
```
public boolean nextResult()
```


Bewegt den [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) zum nächsten Resultatset, falls vorhanden.

**Returns:**
boolean - true, wenn ein weiteres Ergebnis‑Set vorhanden war; andernfalls false.
### read() {#read}
```
public boolean read()
```


Bewegt den [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) zum nächsten Datensatz.

**Returns:**
boolean - true, wenn eine weitere Zeile zum Lesen vorhanden war; andernfalls false.
