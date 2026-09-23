---
title: "CsvDataSource"
linktitle: "CsvDataSource"
second_title: "Aspose.Words für Java"
description: "Stellt Zugriff auf Daten einer CSV-Datei oder eines Streams bereit, die in einem Bericht in Java verwendet werden."
type: docs
weight: 138
url: /de/java/com.aspose.words/csvdatasource/
---

**Inheritance:**
java.lang.Object
```
public class CsvDataSource
```

Bietet Zugriff auf die Daten einer CSV‑Datei oder eines Streams, die in einem Bericht verwendet werden sollen.

Weitere Informationen finden Sie im Dokumentationsartikel zum [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Um Daten der entsprechenden Datei oder des Streams beim Erstellen eines Berichts zuzugreifen, übergeben Sie eine Instanz dieser Klasse als Datenquelle an einen der [ReportingEngine](../../com.aspose.words/reportingengine/) Methoden. Überladungen von buildReport.

In Vorlagendokumenten sollte eine [CsvDataSource](../../com.aspose.words/csvdatasource/) Instanz genauso behandelt werden, als wäre sie eine [DataTable](../../com.aspose.words.net.system.data/datatable/) Instanz. Weitere Informationen finden Sie in der Referenz zur Vorlagensyntax(https://docs.aspose.com/display/wordsjava/Template+Syntax).

Datentypen von kommagetrennten Werten werden automatisch anhand ihrer Zeichenkettenrepräsentationen ermittelt. In Vorlagendokumenten können Sie daher mit typisierten Werten statt nur Zeichenketten arbeiten. Die Engine ist in der Lage, Werte der folgenden Typen automatisch zu erkennen:

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

Beachten Sie, dass für die automatische Erkennung von Datentypen die Zeichenkettenrepräsentationen kommagetrennter Werte mit invariantem Kulturformat erstellt werden müssen.

Um das Standardverhalten beim Laden von CSV-Daten zu überschreiben, initialisieren Sie eine [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) Instanz und übergeben Sie sie dem Konstruktor dieser Klasse.

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
| [CsvDataSource(String csvPath)](#CsvDataSource-java.lang.String) | Erstellt eine neue Datenquelle mit Daten aus einer CSV-Datei unter Verwendung der Standardoptionen zum Parsen von CSV-Daten. |
| [CsvDataSource(String csvPath, CsvDataLoadOptions options)](#CsvDataSource-java.lang.String-com.aspose.words.CsvDataLoadOptions) | Erstellt eine neue Datenquelle mit Daten aus einer CSV-Datei unter Verwendung der angegebenen Optionen zum Parsen von CSV-Daten. |
| [CsvDataSource(InputStream csvStream)](#CsvDataSource-java.io.InputStream) | Initialisiert eine neue Instanz dieser Klasse. |
| [CsvDataSource(InputStream csvStream, CsvDataLoadOptions options)](#CsvDataSource-java.io.InputStream-com.aspose.words.CsvDataLoadOptions) | Initialisiert eine neue Instanz dieser Klasse. |
### CsvDataSource(String csvPath) {#CsvDataSource-java.lang.String}
```
public CsvDataSource(String csvPath)
```


Erstellt eine neue Datenquelle mit Daten aus einer CSV-Datei unter Verwendung der Standardoptionen zum Parsen von CSV-Daten.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| csvPath | java.lang.String | Der Pfad zur CSV-Datei, die als Datenquelle verwendet werden soll. |

### CsvDataSource(String csvPath, CsvDataLoadOptions options) {#CsvDataSource-java.lang.String-com.aspose.words.CsvDataLoadOptions}
```
public CsvDataSource(String csvPath, CsvDataLoadOptions options)
```


Erstellt eine neue Datenquelle mit Daten aus einer CSV-Datei unter Verwendung der angegebenen Optionen zum Parsen von CSV-Daten.

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
| csvPath | java.lang.String | Der Pfad zur CSV-Datei, die als Datenquelle verwendet werden soll. |
| options | [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) | Optionen zum Parsen der CSV-Daten. |

### CsvDataSource(InputStream csvStream) {#CsvDataSource-java.io.InputStream}
```
public CsvDataSource(InputStream csvStream)
```


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| csvStream | java.io.InputStream |  |

### CsvDataSource(InputStream csvStream, CsvDataLoadOptions options) {#CsvDataSource-java.io.InputStream-com.aspose.words.CsvDataLoadOptions}
```
public CsvDataSource(InputStream csvStream, CsvDataLoadOptions options)
```


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| csvStream | java.io.InputStream |  |
| options | [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) |  |

