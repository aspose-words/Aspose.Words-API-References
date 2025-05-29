---
title: JsonDataLoadOptions.ExactDateTimeParseFormats
linktitle: ExactDateTimeParseFormats
articleTitle: ExactDateTimeParseFormats
second_title: Aspose.Words för .NET
description: Upptäck JsonDataLoadOptions ExactDateTimeParseFormats för exakt JSON-datum- och tidsanalys. Anpassa format enkelt för sömlös datainläsning!
type: docs
weight: 30
url: /sv/net/aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/
---
## JsonDataLoadOptions.ExactDateTimeParseFormats property

Hämtar eller ställer in exakta format för att analysera JSON-datum-tidsvärden vid laddning av JSON. Standardinställningen är`null` .

```csharp
public IEnumerable<string> ExactDateTimeParseFormats { get; set; }
```

## Anmärkningar

Strängar kodade med Microsoft® JSON datum- och tidsformat (till exempel "/Date(1224043200000)/") känns alltid igen som datum- och tidsvärden oavsett ett värde för den här egenskapen. Egenskapen definierar ytterligare format som ska användas vid parsning av datum- och tidsvärden från strängar på följande sätt:

* När`ExactDateTimeParseFormats` är`null` , ISO-8601-formatet och alla datum- och tidsformat som stöds för nuvarande, engelsk amerikansk och engelsk nyzeeländsk kultur används dessutom i nämnda ordning.
* När`ExactDateTimeParseFormats`innehåller strängar, används de som ytterligare date-time -format med hjälp av den aktuella kulturen.
* När`ExactDateTimeParseFormats` är tomt, inga ytterligare datum- och tidsformat används.

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
