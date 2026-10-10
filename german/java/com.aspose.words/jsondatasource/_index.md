---
title: "JsonDataSource"
linktitle: "JsonDataSource"
second_title: "Aspose.Words für Java"
description: "Stellt Zugriff auf Daten einer JSON-Datei oder eines Streams bereit, die in einem Bericht in Java verwendet werden."
type: docs
weight: 409
url: /de/java/com.aspose.words/jsondatasource/
---

**Inheritance:**
java.lang.Object
```
public class JsonDataSource
```

Stellt Zugriff auf Daten einer JSON-Datei oder eines Streams bereit, die in einem Bericht verwendet werden.

Weitere Informationen finden Sie im Dokumentationsartikel zum [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Um Daten der entsprechenden Datei oder des Streams beim Erstellen eines Berichts zuzugreifen, übergeben Sie eine Instanz dieser Klasse als Datenquelle an einen der [ReportingEngine](../../com.aspose.words/reportingengine/) Methoden. Überladungen von buildReport.

In Vorlagendokumenten wird eine [JsonDataSource](../../com.aspose.words/jsondatasource/)‑Instanz, wenn das oberste JSON‑Element ein Array ist, genauso behandelt, als wäre es eine [DataTable](../../com.aspose.words.net.system.data/datatable/)‑Instanz. Wenn das oberste JSON‑Element ein Objekt ist, wird eine [JsonDataSource](../../com.aspose.words/jsondatasource/)‑Instanz genauso behandelt, als wäre es eine [DataRow](../../com.aspose.words.net.system.data/datarow/)‑Instanz. Weitere Informationen finden Sie in der Referenz zur Vorlagensyntax(https://docs.aspose.com/display/wordsjava/Template+Syntax).

In Vorlagendokumenten können Sie mit typisierten Werten von JSON‑Elementen arbeiten. Der Engine ersetzt zur Vereinfachung die Menge der einfachen JSON‑Typen durch die folgende:

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

Die Engine erkennt automatisch Werte der zusätzlichen Typen anhand ihrer JSON‑Darstellungen.

Um das Standardverhalten beim Laden von JSON‑Daten zu überschreiben, initialisieren Sie eine [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/)‑Instanz und übergeben sie dem Konstruktor dieser Klasse.

 **Examples:** 

Zeigt, wie man JSON als Datenquelle (String) verwendet.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - JSON data destination (Java).docx");

 JsonDataLoadOptions options = new JsonDataLoadOptions();
 {
     options.setExactDateTimeParseFormats(Arrays.asList(new String[]{"MM/dd/yyyy", "MM.d.yy", "MM d yy"}));
 }

 JsonDataSource dataSource = new JsonDataSource(getMyDir() + "List of people.json", options);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.JsonDataString.docx");
 
```


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [JsonDataSource(String jsonPath)](#JsonDataSource-java.lang.String) | Erstellt eine neue Datenquelle mit Daten aus einer JSON‑Datei unter Verwendung der Standardoptionen zum Parsen von JSON‑Daten. |
| [JsonDataSource(InputStream jsonStream)](#JsonDataSource-java.io.InputStream) | Initialisiert eine neue Instanz dieser Klasse. |
| [JsonDataSource(String jsonPath, JsonDataLoadOptions options)](#JsonDataSource-java.lang.String-com.aspose.words.JsonDataLoadOptions) | Erstellt eine neue Datenquelle mit Daten aus einer JSON‑Datei unter Verwendung der angegebenen Optionen zum Parsen von JSON‑Daten. |
| [JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options)](#JsonDataSource-java.io.InputStream-com.aspose.words.JsonDataLoadOptions) | Initialisiert eine neue Instanz dieser Klasse. |
### JsonDataSource(String jsonPath) {#JsonDataSource-java.lang.String}
```
public JsonDataSource(String jsonPath)
```


Erstellt eine neue Datenquelle mit Daten aus einer JSON‑Datei unter Verwendung der Standardoptionen zum Parsen von JSON‑Daten.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| jsonPath | java.lang.String | Der Pfad zur JSON‑Datei, die als Datenquelle verwendet werden soll. |

### JsonDataSource(InputStream jsonStream) {#JsonDataSource-java.io.InputStream}
```
public JsonDataSource(InputStream jsonStream)
```


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| jsonStream | java.io.InputStream |  |

### JsonDataSource(String jsonPath, JsonDataLoadOptions options) {#JsonDataSource-java.lang.String-com.aspose.words.JsonDataLoadOptions}
```
public JsonDataSource(String jsonPath, JsonDataLoadOptions options)
```


Erstellt eine neue Datenquelle mit Daten aus einer JSON‑Datei unter Verwendung der angegebenen Optionen zum Parsen von JSON‑Daten.

 **Examples:** 

Zeigt, wie man JSON als Datenquelle (String) verwendet.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - JSON data destination (Java).docx");

 JsonDataLoadOptions options = new JsonDataLoadOptions();
 {
     options.setExactDateTimeParseFormats(Arrays.asList(new String[]{"MM/dd/yyyy", "MM.d.yy", "MM d yy"}));
 }

 JsonDataSource dataSource = new JsonDataSource(getMyDir() + "List of people.json", options);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.JsonDataString.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| jsonPath | java.lang.String | Der Pfad zur JSON‑Datei, die als Datenquelle verwendet werden soll. |
| options | [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) | Optionen zum Parsen von JSON‑Daten. |

### JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options) {#JsonDataSource-java.io.InputStream-com.aspose.words.JsonDataLoadOptions}
```
public JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options)
```


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| jsonStream | java.io.InputStream |  |
| options | [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) |  |

