---
title: JsonDataLoadOptions
linktitle: JsonDataLoadOptions
articleTitle: JsonDataLoadOptions
second_title: Aspose.Words för .NET
description: Upptäck JsonDataLoadOptions-konstruktorn och initiera enkelt din datainläsning med anpassningsbara standardinställningar för optimal prestanda.
type: docs
weight: 10
url: /sv/net/aspose.words.reporting/jsondataloadoptions/jsondataloadoptions/
---
## JsonDataLoadOptions constructor

Initierar en ny instans av den här klassen med standardalternativ.

```csharp
public JsonDataLoadOptions()
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

* class [JsonDataLoadOptions](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)
