---
title: JsonDataLoadOptions.SimpleValueParseMode
linktitle: SimpleValueParseMode
articleTitle: SimpleValueParseMode
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen SimpleValueParseMode i JsonDataLoadOptions förbättrar JSON-parsning för nullvärden, booleska värden, tal och strängar. Optimera din datainläsning idag!
type: docs
weight: 50
url: /sv/net/aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/
---
## JsonDataLoadOptions.SimpleValueParseMode property

Hämtar eller ställer in ett läge för att analysera enkla JSON-värden (null, booleska, tal, heltal och sträng) vid laddning av JSON. Ett sådant läge påverkar inte analyseringen av datum-tid-värden. Standardvärdet är Loose .

```csharp
public JsonSimpleValueParseMode SimpleValueParseMode { get; set; }
```

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

* enum [JsonSimpleValueParseMode](../../jsonsimplevalueparsemode/)
* class [JsonDataLoadOptions](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)
