---
title: CsvDataLoadOptions.Delimiter
linktitle: Delimiter
articleTitle: Delimiter
second_title: Aspose.Words för .NET
description: Upptäck egenskapen CsvDataLoadOptions Delimiter för att enkelt anpassa kolumnavgränsare för effektiv datainläsning. Optimera din datahantering idag!
type: docs
weight: 30
url: /sv/net/aspose.words.reporting/csvdataloadoptions/delimiter/
---
## CsvDataLoadOptions.Delimiter property

Hämtar eller anger tecknet som ska användas som kolumnavgränsare.

```csharp
public char Delimiter { get; set; }
```

## Anmärkningar

Standardvärdet är ',' (komma).

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

* class [CsvDataLoadOptions](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)
