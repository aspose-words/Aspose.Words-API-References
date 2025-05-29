---
title: XmlDataSource
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: Aspose.Words für .NET
description: Erstellen Sie mühelos eine leistungsstarke Datenquelle mit dem XmlDataSource-Konstruktor und laden Sie XML-Daten mit optimierten Standardoptionen für eine nahtlose Integration.
type: docs
weight: 10
url: /de/net/aspose.words.reporting/xmldatasource/xmldatasource/
---
## XmlDataSource(*string*) {#constructor_4}

Erstellt eine neue Datenquelle mit Daten aus einer XML-Datei unter Verwendung der Standardoptionen zum Laden von XML-Daten.

```csharp
public XmlDataSource(string xmlPath)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xmlPath | String | Der Pfad zur XML-Datei, die als Datenquelle verwendet werden soll. |

## Beispiele

Zeigen Sie, wie XML als Datenquelle (Zeichenfolge) verwendet wird.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

XmlDataSource dataSource = new XmlDataSource(MyDir + "List of people.xml");
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataString.docx");
```

### Siehe auch

* class [XmlDataSource](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)

---

## XmlDataSource(*Stream*) {#constructor}

Erstellt eine neue Datenquelle mit Daten aus einem XML-Stream unter Verwendung der Standardoptionen zum Laden von XML-Daten.

```csharp
public XmlDataSource(Stream xmlStream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xmlStream | Stream | Der XML-Datenstrom, der als Datenquelle verwendet werden soll. |

## Beispiele

Zeigen Sie, wie XML als Datenquelle (Stream) verwendet wird.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

using (FileStream stream = File.OpenRead(MyDir + "List of people.xml"))
{
    XmlDataSource dataSource = new XmlDataSource(stream);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataStream.docx");
```

### Siehe auch

* class [XmlDataSource](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)

---

## XmlDataSource(*string, string*) {#constructor_6}

Erstellt eine neue Datenquelle mit Daten aus einer XML-Datei unter Verwendung einer XML-Schemadefinitionsdatei. Zum Laden von XML-Daten werden die Standardoptionen verwendet.

```csharp
public XmlDataSource(string xmlPath, string xmlSchemaPath)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xmlPath | String | Der Pfad zur XML-Datei, die als Datenquelle verwendet werden soll. |
| xmlSchemaPath | String | Der Pfad zur XML-Schemadefinitionsdatei, die das Schema für die XML -Datei bereitstellt. |

### Siehe auch

* class [XmlDataSource](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, Stream*) {#constructor_2}

Erstellt eine neue Datenquelle mit Daten aus einem XML-Stream unter Verwendung eines XML-Schemadefinitionsstreams. Zum Laden der XML-Daten werden die Standardoptionen verwendet.

```csharp
public XmlDataSource(Stream xmlStream, Stream xmlSchemaStream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xmlStream | Stream | Der XML-Datenstrom, der als Datenquelle verwendet werden soll. |
| xmlSchemaStream | Stream | Der Stream der XML-Schemadefinition, der das Schema für die XML-Daten bereitstellt. |

### Siehe auch

* class [XmlDataSource](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)

---

## XmlDataSource(*string, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_5}

Erstellt eine neue Datenquelle mit Daten aus einer XML-Datei unter Verwendung der angegebenen Optionen zum Laden von XML-Daten.

```csharp
public XmlDataSource(string xmlPath, XmlDataLoadOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xmlPath | String | Der Pfad zur XML-Datei, die als Datenquelle verwendet werden soll. |
| options | XmlDataLoadOptions | Optionen zum Laden von XML-Daten. |

### Siehe auch

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_1}

Erstellt eine neue Datenquelle mit Daten aus einem XML-Stream unter Verwendung der angegebenen Optionen zum Laden von XML-Daten.

```csharp
public XmlDataSource(Stream xmlStream, XmlDataLoadOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xmlStream | Stream | Der XML-Datenstrom, der als Datenquelle verwendet werden soll. |
| options | XmlDataLoadOptions | Optionen zum Laden von XML-Daten. |

### Siehe auch

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)

---

## XmlDataSource(*string, string, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_7}

Erstellt eine neue Datenquelle mit Daten aus einer XML-Datei unter Verwendung einer XML-Schemadefinitionsdatei. Die angegebenen Optionen werden zum Laden der XML-Daten verwendet.

```csharp
public XmlDataSource(string xmlPath, string xmlSchemaPath, XmlDataLoadOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xmlPath | String | Der Pfad zur XML-Datei, die als Datenquelle verwendet werden soll. |
| xmlSchemaPath | String | Der Pfad zur XML-Schemadefinitionsdatei, die das Schema für die XML -Datei bereitstellt. |
| options | XmlDataLoadOptions | Optionen zum Laden von XML-Daten. |

### Siehe auch

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, Stream, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_3}

Erstellt eine neue Datenquelle mit Daten aus einem XML-Stream unter Verwendung eines XML-Schemadefinitionsstreams. Die angegebenen Optionen werden zum Laden der XML-Daten verwendet.

```csharp
public XmlDataSource(Stream xmlStream, Stream xmlSchemaStream, XmlDataLoadOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xmlStream | Stream | Der XML-Datenstrom, der als Datenquelle verwendet werden soll. |
| xmlSchemaStream | Stream | Der Stream der XML-Schemadefinition, der das Schema für die XML-Daten bereitstellt. |
| options | XmlDataLoadOptions | Optionen zum Laden von XML-Daten. |

### Siehe auch

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)
