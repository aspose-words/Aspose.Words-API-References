---
title: JsonDataLoadOptions Class
linktitle: JsonDataLoadOptions
articleTitle: JsonDataLoadOptions
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Reporting.JsonDataLoadOptions för sömlös JSON-dataparsning. Förbättra din dokumentbehandling med flexibla alternativ!
type: docs
weight: 5420
url: /sv/net/aspose.words.reporting/jsondataloadoptions/
---
## JsonDataLoadOptions class

Representerar alternativ för att analysera JSON-data.

För att lära dig mer, besök[LINQ-rapporteringsmotor](https://docs.aspose.com/words/net/linq-reporting-engine/) dokumentationsartikel.

```csharp
public class JsonDataLoadOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [JsonDataLoadOptions](jsondataloadoptions/)() | Initierar en ny instans av den här klassen med standardalternativ. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AlwaysGenerateRootObject](../../aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/) { get; set; } | Hämtar eller ställer in en flagga som anger om en genererad datakälla alltid kommer att innehålla ett objekt för ett JSON root -element. Om ett JSON-rotelement innehåller en enda komplex egenskap skapas inte ett sådant objekt som standard. |
| [ExactDateTimeParseFormats](../../aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/) { get; set; } | Hämtar eller ställer in exakta format för att analysera JSON-datum-tidsvärden vid laddning av JSON. Standardinställningen är`null` . |
| [PreserveSpaces](../../aspose.words.reporting/jsondataloadoptions/preservespaces/) { get; set; } | Hämtar eller anger en flagga som anger om inledande och efterföljande mellanslag ska bevaras när string -värden för JSON-data laddas. |
| [SimpleValueParseMode](../../aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/) { get; set; } | Hämtar eller ställer in ett läge för att analysera enkla JSON-värden (null, booleska, tal, heltal och sträng) vid laddning av JSON. Ett sådant läge påverkar inte analyseringen av datum-tid-värden. Standardvärdet är Loose . |

## Anmärkningar

En instans av den här klassen kan skickas till konstruktorer av[`JsonDataSource`](../jsondatasource/) .

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
