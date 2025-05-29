---
title: CsvDataLoadOptions Class
linktitle: CsvDataLoadOptions
articleTitle: CsvDataLoadOptions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Reporting.CsvDataLoadOptions för effektiv CSV-dataparsning. Optimera din dokumenthantering med anpassningsbara alternativ idag!
type: docs
weight: 5400
url: /sv/net/aspose.words.reporting/csvdataloadoptions/
---
## CsvDataLoadOptions class

Representerar alternativ för att analysera CSV-data.

För att lära dig mer, besök[LINQ-rapporteringsmotor](https://docs.aspose.com/words/net/linq-reporting-engine/) dokumentationsartikel.

```csharp
public class CsvDataLoadOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [CsvDataLoadOptions](csvdataloadoptions/#constructor)() | Initierar en ny instans av den här klassen med standardalternativ. |
| [CsvDataLoadOptions](csvdataloadoptions/#constructor_1)(*bool*) | Initierar en ny instans av denna klass genom att ange om CSV-data innehåller kolumnnamnen på första raden. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CommentChar](../../aspose.words.reporting/csvdataloadoptions/commentchar/) { get; set; } | Hämtar eller anger tecknet som används för att kommentera rader med CSV-data. |
| [Delimiter](../../aspose.words.reporting/csvdataloadoptions/delimiter/) { get; set; } | Hämtar eller anger tecknet som ska användas som kolumnavgränsare. |
| [HasHeaders](../../aspose.words.reporting/csvdataloadoptions/hasheaders/) { get; set; } | Hämtar eller anger ett värde som anger om den första posten med CSV-data innehåller kolumnnamn. |
| [QuoteChar](../../aspose.words.reporting/csvdataloadoptions/quotechar/) { get; set; } | Hämtar eller anger tecknet som används för att citera fältvärden. |

## Anmärkningar

En instans av den här klassen kan skickas till konstruktorer av[`CsvDataSource`](../csvdatasource/) .

## Exempel

Visar hur man använder CSV som datakälla (sträng).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - CSV data destination.docx");

CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
loadOptions.Delimiter = ';';
loadOptions.CommentChar = '$';
loadOptions.HasHeaders = true;
loadOptions.QuoteChar = '"';

CsvDataSource dataSource = new CsvDataSource(MyDir + "List of people.csv", loadOptions);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.CsvDataString.docx");
```

### Se även

* namnutrymme [Aspose.Words.Reporting](../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../)
