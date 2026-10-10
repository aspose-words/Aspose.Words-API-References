---
title: "CsvDataLoadOptions"
linktitle: "CsvDataLoadOptions"
second_title: "Aspose.Words für Java"
description: "Stellt Optionen zum Parsen von CSV-Daten in Java dar."
type: docs
weight: 137
url: /de/java/com.aspose.words/csvdataloadoptions/
---

**Inheritance:**
java.lang.Object
```
public class CsvDataLoadOptions
```

Stellt Optionen für das Parsen von CSV‑Daten dar.

Weitere Informationen finden Sie im Dokumentationsartikel zum [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Eine Instanz dieser Klasse kann an die Konstruktoren von [CsvDataSource](../../com.aspose.words/csvdatasource/) übergeben werden.

 **Examples:** 

Zeigt, wie CSV als Datenquelle (String) verwendet wird.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [CsvDataLoadOptions()](#CsvDataLoadOptions) | Initialisiert eine neue Instanz dieser Klasse mit Standardoptionen. |
| [CsvDataLoadOptions(boolean hasHeaders)](#CsvDataLoadOptions-boolean) | Initialisiert eine neue Instanz dieser Klasse und gibt an, ob CSV-Daten in der ersten Zeile Spaltennamen enthalten. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getCommentChar()](#getCommentChar) | Gibt das Zeichen zurück, das zum Kommentieren von Zeilen in CSV-Daten verwendet wird. |
| [getDelimiter()](#getDelimiter) | Gibt das Zeichen zurück, das als Spaltentrennzeichen verwendet wird. |
| [getQuoteChar()](#getQuoteChar) | Gibt das Zeichen zurück, das zum Anführen von Feldwerten verwendet wird. |
| [hasHeaders()](#hasHeaders) | Gibt einen Wert zurück, der angibt, ob der erste Datensatz der CSV-Daten Spaltennamen enthält. |
| [hasHeaders(boolean value)](#hasHeaders-boolean) | Legt einen Wert fest, der angibt, ob der erste Datensatz der CSV-Daten Spaltennamen enthält. |
| [setCommentChar(char value)](#setCommentChar-char) | Legt das Zeichen fest, das zum Kommentieren von Zeilen in CSV-Daten verwendet wird. |
| [setDelimiter(char value)](#setDelimiter-char) | Legt das Zeichen fest, das als Spaltentrennzeichen verwendet wird. |
| [setQuoteChar(char value)](#setQuoteChar-char) | Legt das Zeichen fest, das zum Anführen von Feldwerten verwendet wird. |
### CsvDataLoadOptions() {#CsvDataLoadOptions}
```
public CsvDataLoadOptions()
```


Initialisiert eine neue Instanz dieser Klasse mit Standardoptionen.

 **Examples:** 

Zeigt, wie CSV als Datenquelle (String) verwendet wird.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

### CsvDataLoadOptions(boolean hasHeaders) {#CsvDataLoadOptions-boolean}
```
public CsvDataLoadOptions(boolean hasHeaders)
```


Initialisiert eine neue Instanz dieser Klasse und gibt an, ob CSV-Daten in der ersten Zeile Spaltennamen enthalten.

 **Examples:** 

Zeigt, wie CSV als Datenquelle (String) verwendet wird.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| hasHeaders | boolean |  |

### getCommentChar() {#getCommentChar}
```
public char getCommentChar()
```


Gibt das Zeichen zurück, das zum Kommentieren von Zeilen in CSV-Daten verwendet wird.

 **Remarks:** 

Der Standardwert ist '\#' (Raute).

 **Examples:** 

Zeigt, wie CSV als Datenquelle (String) verwendet wird.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Returns:**
char - Das Zeichen, das zum Kommentieren von Zeilen in CSV-Daten verwendet wird.
### getDelimiter() {#getDelimiter}
```
public char getDelimiter()
```


Gibt das Zeichen zurück, das als Spaltentrennzeichen verwendet wird.

 **Remarks:** 

Der Standardwert ist ',' (Komma).

 **Examples:** 

Zeigt, wie CSV als Datenquelle (String) verwendet wird.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Returns:**
char - Das Zeichen, das als Spaltentrennzeichen verwendet wird.
### getQuoteChar() {#getQuoteChar}
```
public char getQuoteChar()
```


Gibt das Zeichen zurück, das zum Anführen von Feldwerten verwendet wird.

 **Remarks:** 

Der Standardwert ist '"' (Anführungszeichen).

Verdoppeln Sie das Zeichen, um es in einen zitierten Text einzufügen.

 **Examples:** 

Zeigt, wie CSV als Datenquelle (String) verwendet wird.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Returns:**
char - Das Zeichen, das zum Anführen von Feldwerten verwendet wird.
### hasHeaders() {#hasHeaders}
```
public boolean hasHeaders()
```


Gibt einen Wert zurück, der angibt, ob der erste Datensatz der CSV-Daten Spaltennamen enthält.

 **Remarks:** 

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie CSV als Datenquelle (String) verwendet wird.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Returns:**
boolean - Ein Wert, der angibt, ob der erste Datensatz der CSV-Daten Spaltennamen enthält.
### hasHeaders(boolean value) {#hasHeaders-boolean}
```
public void hasHeaders(boolean value)
```


Legt einen Wert fest, der angibt, ob der erste Datensatz der CSV-Daten Spaltennamen enthält.

 **Remarks:** 

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie CSV als Datenquelle (String) verwendet wird.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Wert, der angibt, ob der erste Datensatz von CSV-Daten Spaltennamen enthält. |

### setCommentChar(char value) {#setCommentChar-char}
```
public void setCommentChar(char value)
```


Legt das Zeichen fest, das zum Kommentieren von Zeilen in CSV-Daten verwendet wird.

 **Remarks:** 

Der Standardwert ist '\#' (Raute).

 **Examples:** 

Zeigt, wie CSV als Datenquelle (String) verwendet wird.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | char | Das Zeichen, das verwendet wird, um Zeilen von CSV-Daten zu kommentieren. |

### setDelimiter(char value) {#setDelimiter-char}
```
public void setDelimiter(char value)
```


Legt das Zeichen fest, das als Spaltentrennzeichen verwendet wird.

 **Remarks:** 

Der Standardwert ist ',' (Komma).

 **Examples:** 

Zeigt, wie CSV als Datenquelle (String) verwendet wird.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | char | Das Zeichen, das als Spaltentrennzeichen verwendet werden soll. |

### setQuoteChar(char value) {#setQuoteChar-char}
```
public void setQuoteChar(char value)
```


Legt das Zeichen fest, das zum Anführen von Feldwerten verwendet wird.

 **Remarks:** 

Der Standardwert ist '"' (Anführungszeichen).

Verdoppeln Sie das Zeichen, um es in einen zitierten Text einzufügen.

 **Examples:** 

Zeigt, wie CSV als Datenquelle (String) verwendet wird.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | char | Das Zeichen, das zum Anführen von Feldwerten verwendet wird. |

