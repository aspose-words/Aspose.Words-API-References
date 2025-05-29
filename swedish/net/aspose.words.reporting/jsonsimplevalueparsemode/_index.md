---
title: JsonSimpleValueParseMode Enum
linktitle: JsonSimpleValueParseMode
articleTitle: JsonSimpleValueParseMode
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Reporting.JsonSimpleValueParseMode-enum för effektiv JSON-parsning. Hantera enkelt nullvärden, booleska värden, tal och strängar sömlöst!
type: docs
weight: 5440
url: /sv/net/aspose.words.reporting/jsonsimplevalueparsemode/
---
## JsonSimpleValueParseMode enumeration

Anger ett läge för att analysera enkla JSON-värden (null, booleska, tal, heltal och sträng) vid laddning av JSON. Ett sådant läge påverkar inte analysering av datum- och tidsvärden.

```csharp
public enum JsonSimpleValueParseMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Loose | `0` | Anger läget där typer av enkla JSON-värden bestäms vid parsning av deras strängrepresentationer. Till exempel bestäms typen av 'prop' från JSON-kodavsnittet '{ prop: "123" }' som ett heltal i detta läge. |
| Strict | `1` | Anger läget där typer av enkla JSON-värden bestäms från själva JSON-notationen. Till exempel bestäms typen av 'prop' från JSON-kodavsnittet '{ prop: "123" }' som sträng i detta läge. |

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

* namnutrymme [Aspose.Words.Reporting](../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../)
