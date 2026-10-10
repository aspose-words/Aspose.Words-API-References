---
title: "XmlDataSource"
linktitle: "XmlDataSource"
second_title: "Aspose.Words für Java"
description: "Stellt Zugriff auf Daten einer XML‑Datei oder eines Streams bereit, die in einem Bericht in Java verwendet werden."
type: docs
weight: 746
url: /de/java/com.aspose.words/xmldatasource/
---

**Inheritance:**
java.lang.Object
```
public class XmlDataSource
```

Stellt Zugriff auf Daten einer XML-Datei oder eines Streams bereit, die innerhalb eines Berichts verwendet werden.

Weitere Informationen finden Sie im Dokumentationsartikel zum [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Um Daten der entsprechenden Datei oder des Streams beim Erstellen eines Berichts zuzugreifen, übergeben Sie eine Instanz dieser Klasse als Datenquelle an einen der [ReportingEngine](../../com.aspose.words/reportingengine/) Methoden. Überladungen von buildReport.

In Vorlagendokumenten sollte, wenn ein XML‑Element der obersten Ebene nur eine Liste von Elementen desselben Typs enthält, eine [XmlDataSource](../../com.aspose.words/xmldatasource/)‑Instanz so behandelt werden, als wäre sie eine [DataTable](../../com.aspose.words.net.system.data/datatable/)‑Instanz. Andernfalls sollte eine [XmlDataSource](../../com.aspose.words/xmldatasource/)‑Instanz so behandelt werden, als wäre sie eine [DataRow](../../com.aspose.words.net.system.data/datarow/)‑Instanz. Weitere Informationen finden Sie in der Referenz(https://docs.aspose.com/display/wordsjava/Template+Syntax).

Wenn eine XML‑Schema‑Definition an den Konstruktor dieser Klasse übergeben wird, werden die Datentypen der Werte einfacher XML‑Elemente und Attribute gemäß dem Schema bestimmt. In Vorlagendokumenten können Sie daher mit typisierten Werten statt nur mit Zeichenketten arbeiten.

Wenn keine XML‑Schema‑Definition an den Konstruktor dieser Klasse übergeben wird, werden die Datentypen der Werte einfacher XML‑Elemente und Attribute automatisch anhand ihrer Zeichenkettenrepräsentationen bestimmt. In Vorlagendokumenten können Sie in diesem Fall ebenfalls mit typisierten Werten arbeiten. Die Engine ist in der Lage, Werte der folgenden Typen automatisch zu erkennen:

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

Beachten Sie, dass für die automatische Erkennung von Datentypen die Zeichenkettenrepräsentationen der Werte einfacher XML‑Elemente und Attribute mit invarianten Kultureinstellungen erstellt werden sollten.

Um das Standardverhalten beim Laden von XML‑Daten zu überschreiben, initialisieren Sie eine [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/)‑Instanz und übergeben sie dem Konstruktor dieser Klasse.

 **Examples:** 

Zeigt, wie XML als Datenquelle (String) verwendet wird.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - XML data destination (Java).docx");

 XmlDataSource dataSource = new XmlDataSource(getMyDir() + "List of people.xml");
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.XmlDataString.docx");
 
```

Zeigt, wie XML als Datenquelle (Stream) verwendet wird.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - XML data destination (Java).docx");

 InputStream stream = new FileInputStream(getMyDir() + "List of people.xml");
 try {
     XmlDataSource dataSource = new XmlDataSource(stream);
     buildReport(doc, dataSource, "persons");
 } finally {
     stream.close();
 }

 doc.save(getArtifactsDir() + "ReportingEngine.XmlDataStream.docx");
 
```


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [XmlDataSource(String xmlPath)](#XmlDataSource-java.lang.String) | Erstellt eine neue Datenquelle mit Daten aus einer XML‑Datei unter Verwendung der Standardoptionen für das Laden von XML‑Daten. |
| [XmlDataSource(InputStream xmlStream)](#XmlDataSource-java.io.InputStream) | Initialisiert eine neue Instanz dieser Klasse. |
| [XmlDataSource(String xmlPath, String xmlSchemaPath)](#XmlDataSource-java.lang.String-java.lang.String) | Erstellt eine neue Datenquelle mit Daten aus einer XML‑Datei unter Verwendung einer XML‑Schema‑Definitionsdatei. |
| [XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream)](#XmlDataSource-java.io.InputStream-java.io.InputStream) | Initialisiert eine neue Instanz dieser Klasse. |
| [XmlDataSource(String xmlPath, XmlDataLoadOptions options)](#XmlDataSource-java.lang.String-com.aspose.words.XmlDataLoadOptions) | Erstellt eine neue Datenquelle mit Daten aus einer XML‑Datei unter Verwendung der angegebenen Optionen für das Laden von XML‑Daten. |
| [XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options)](#XmlDataSource-java.io.InputStream-com.aspose.words.XmlDataLoadOptions) | Initialisiert eine neue Instanz dieser Klasse. |
| [XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options)](#XmlDataSource-java.lang.String-java.lang.String-com.aspose.words.XmlDataLoadOptions) | Erstellt eine neue Datenquelle mit Daten aus einer XML‑Datei unter Verwendung einer XML‑Schema‑Definitionsdatei. |
| [XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options)](#XmlDataSource-java.io.InputStream-java.io.InputStream-com.aspose.words.XmlDataLoadOptions) | Initialisiert eine neue Instanz dieser Klasse. |
### XmlDataSource(String xmlPath) {#XmlDataSource-java.lang.String}
```
public XmlDataSource(String xmlPath)
```


Erstellt eine neue Datenquelle mit Daten aus einer XML‑Datei unter Verwendung der Standardoptionen für das Laden von XML‑Daten.

 **Examples:** 

Zeigt, wie XML als Datenquelle (String) verwendet wird.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - XML data destination (Java).docx");

 XmlDataSource dataSource = new XmlDataSource(getMyDir() + "List of people.xml");
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.XmlDataString.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xmlPath | java.lang.String | Der Pfad zur XML-Datei, die als Datenquelle verwendet wird. |

### XmlDataSource(InputStream xmlStream) {#XmlDataSource-java.io.InputStream}
```
public XmlDataSource(InputStream xmlStream)
```


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |

### XmlDataSource(String xmlPath, String xmlSchemaPath) {#XmlDataSource-java.lang.String-java.lang.String}
```
public XmlDataSource(String xmlPath, String xmlSchemaPath)
```


Erstellt eine neue Datenquelle mit Daten aus einer XML-Datei unter Verwendung einer XML Schema Definition-Datei. Standardoptionen werden für das Laden von XML-Daten verwendet.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xmlPath | java.lang.String | Der Pfad zur XML-Datei, die als Datenquelle verwendet wird. |
| xmlSchemaPath | java.lang.String | Der Pfad zur XML Schema Definition-Datei, die das Schema für die XML-Datei bereitstellt. |

### XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream) {#XmlDataSource-java.io.InputStream-java.io.InputStream}
```
public XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream)
```


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| xmlSchemaStream | java.io.InputStream |  |

### XmlDataSource(String xmlPath, XmlDataLoadOptions options) {#XmlDataSource-java.lang.String-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(String xmlPath, XmlDataLoadOptions options)
```


Erstellt eine neue Datenquelle mit Daten aus einer XML‑Datei unter Verwendung der angegebenen Optionen für das Laden von XML‑Daten.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xmlPath | java.lang.String | Der Pfad zur XML-Datei, die als Datenquelle verwendet wird. |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) | Optionen für das Laden von XML-Daten. |

### XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options) {#XmlDataSource-java.io.InputStream-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options)
```


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) |  |

### XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options) {#XmlDataSource-java.lang.String-java.lang.String-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options)
```


Erstellt eine neue Datenquelle mit Daten aus einer XML-Datei unter Verwendung einer XML Schema Definition-Datei. Die angegebenen Optionen werden für das Laden von XML-Daten verwendet.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xmlPath | java.lang.String | Der Pfad zur XML-Datei, die als Datenquelle verwendet wird. |
| xmlSchemaPath | java.lang.String | Der Pfad zur XML Schema Definition-Datei, die das Schema für die XML-Datei bereitstellt. |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) | Optionen für das Laden von XML-Daten. |

### XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options) {#XmlDataSource-java.io.InputStream-java.io.InputStream-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options)
```


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| xmlSchemaStream | java.io.InputStream |  |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) |  |

