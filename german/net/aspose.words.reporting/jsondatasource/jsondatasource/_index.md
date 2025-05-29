---
title: JsonDataSource
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words für .NET
description: Erstellen Sie mühelos eine leistungsstarke Datenquelle mit dem JsonDataSource-Konstruktor, der eine nahtlose Integration von JSON-Dateien und eine optimierte Datenanalyse ermöglicht.
type: docs
weight: 10
url: /de/net/aspose.words.reporting/jsondatasource/jsondatasource/
---
## JsonDataSource(*string*) {#constructor_2}

Erstellt eine neue Datenquelle mit Daten aus einer JSON-Datei unter Verwendung der Standardoptionen zum Parsen von JSON-Daten.

```csharp
public JsonDataSource(string jsonPath)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| jsonPath | String | Der Pfad zur JSON-Datei, die als Datenquelle verwendet werden soll. |

### Siehe auch

* class [JsonDataSource](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)

---

## JsonDataSource(*Stream*) {#constructor}

Erstellt eine neue Datenquelle mit Daten aus einem JSON-Stream unter Verwendung der Standardoptionen zum Parsen von JSON-Daten.

```csharp
public JsonDataSource(Stream jsonStream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| jsonStream | Stream | Der JSON-Datenstrom, der als Datenquelle verwendet werden soll. |

### Siehe auch

* class [JsonDataSource](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)

---

## JsonDataSource(*string, [JsonDataLoadOptions](../../jsondataloadoptions/)*) {#constructor_3}

Erstellt eine neue Datenquelle mit Daten aus einer JSON-Datei unter Verwendung der angegebenen Optionen zum Parsen von JSON-Daten.

```csharp
public JsonDataSource(string jsonPath, JsonDataLoadOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| jsonPath | String | Der Pfad zur JSON-Datei, die als Datenquelle verwendet werden soll. |
| options | JsonDataLoadOptions | Optionen zum Parsen von JSON-Daten. |

## Beispiele

Zeigt, wie JSON als Datenquelle (Zeichenfolge) verwendet wird.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - JSON data destination.docx");

JsonDataLoadOptions options = new JsonDataLoadOptions
{
    ExactDateTimeParseFormats = new List<string> {"MM/dd/yyyy", "MM.d.yy", "MM d yy"},
    AlwaysGenerateRootObject = true,
    PreserveSpaces = true,
    SimpleValueParseMode = JsonSimpleValueParseMode.Loose
};

JsonDataSource dataSource = new JsonDataSource(MyDir + "List of people.json", options);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.JsonDataString.docx");
```

### Siehe auch

* class [JsonDataLoadOptions](../../jsondataloadoptions/)
* class [JsonDataSource](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)

---

## JsonDataSource(*Stream, [JsonDataLoadOptions](../../jsondataloadoptions/)*) {#constructor_1}

Erstellt eine neue Datenquelle mit Daten aus einem JSON-Stream unter Verwendung der angegebenen Optionen zum Parsen von JSON-Daten.

```csharp
public JsonDataSource(Stream jsonStream, JsonDataLoadOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| jsonStream | Stream | Der JSON-Datenstrom, der als Datenquelle verwendet werden soll. |
| options | JsonDataLoadOptions | Optionen zum Parsen von JSON-Daten. |

## Beispiele

Zeigt, wie JSON als Datenquelle (Stream) verwendet wird.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - JSON data destination.docx");

JsonDataLoadOptions options = new JsonDataLoadOptions
{
    ExactDateTimeParseFormats = new List<string> {"MM/dd/yyyy", "MM.d.yy", "MM d yy"}
};

using (FileStream stream = File.OpenRead(MyDir + "List of people.json"))
{
    JsonDataSource dataSource = new JsonDataSource(stream, options);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.JsonDataStream.docx");
```

### Siehe auch

* class [JsonDataLoadOptions](../../jsondataloadoptions/)
* class [JsonDataSource](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)
