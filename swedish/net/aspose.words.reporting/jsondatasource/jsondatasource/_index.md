---
title: JsonDataSource
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words för .NET
description: Skapa enkelt en kraftfull datakälla med JsonDataSource-konstruktorn, vilket möjliggör sömlös integration av JSON-filer och optimerad dataparsning.
type: docs
weight: 10
url: /sv/net/aspose.words.reporting/jsondatasource/jsondatasource/
---
## JsonDataSource(*string*) {#constructor_2}

Skapar en ny datakälla med data från en JSON-fil med standardalternativ för att analysera JSON-data.

```csharp
public JsonDataSource(string jsonPath)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| jsonPath | String | Sökvägen till JSON-filen som ska användas som datakälla. |

### Se även

* class [JsonDataSource](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)

---

## JsonDataSource(*Stream*) {#constructor}

Skapar en ny datakälla med data från en JSON-ström med standardalternativ för att analysera JSON-data.

```csharp
public JsonDataSource(Stream jsonStream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| jsonStream | Stream | Den JSON-dataström som ska användas som datakälla. |

### Se även

* class [JsonDataSource](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)

---

## JsonDataSource(*string, [JsonDataLoadOptions](../../jsondataloadoptions/)*) {#constructor_3}

Skapar en ny datakälla med data från en JSON-fil med hjälp av de angivna alternativen för att analysera JSON-data.

```csharp
public JsonDataSource(string jsonPath, JsonDataLoadOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| jsonPath | String | Sökvägen till JSON-filen som ska användas som datakälla. |
| options | JsonDataLoadOptions | Alternativ för att analysera JSON-data. |

## Exempel

Visar hur man använder JSON som datakälla (sträng).

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

### Se även

* class [JsonDataLoadOptions](../../jsondataloadoptions/)
* class [JsonDataSource](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)

---

## JsonDataSource(*Stream, [JsonDataLoadOptions](../../jsondataloadoptions/)*) {#constructor_1}

Skapar en ny datakälla med data från en JSON-ström med hjälp av de angivna alternativen för att analysera JSON-data.

```csharp
public JsonDataSource(Stream jsonStream, JsonDataLoadOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| jsonStream | Stream | Den JSON-dataström som ska användas som datakälla. |
| options | JsonDataLoadOptions | Alternativ för att analysera JSON-data. |

## Exempel

Visar hur man använder JSON som datakälla (ström).

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

### Se även

* class [JsonDataLoadOptions](../../jsondataloadoptions/)
* class [JsonDataSource](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)
