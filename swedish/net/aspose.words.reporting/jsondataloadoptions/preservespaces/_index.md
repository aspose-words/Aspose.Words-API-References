---
title: JsonDataLoadOptions.PreserveSpaces
linktitle: PreserveSpaces
articleTitle: PreserveSpaces
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen JsonDataLoadOptions PreserveSpaces förbättrar JSON-datahanteringen genom att bevara inledande och efterföljande mellanslag för korrekta strängvärden.
type: docs
weight: 40
url: /sv/net/aspose.words.reporting/jsondataloadoptions/preservespaces/
---
## JsonDataLoadOptions.PreserveSpaces property

Hämtar eller anger en flagga som anger om inledande och efterföljande mellanslag ska bevaras när string -värden för JSON-data laddas.

```csharp
public bool PreserveSpaces { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk` .

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
