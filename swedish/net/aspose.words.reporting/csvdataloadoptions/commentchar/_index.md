---
title: CsvDataLoadOptions.CommentChar
linktitle: CommentChar
articleTitle: CommentChar
second_title: Aspose.Words för .NET
description: Upptäck hur du anpassar CommentChar-egenskapen i CsvDataLoadOptions för att förbättra din CSV-datahantering. Optimera din datainläsning idag!
type: docs
weight: 20
url: /sv/net/aspose.words.reporting/csvdataloadoptions/commentchar/
---
## CsvDataLoadOptions.CommentChar property

Hämtar eller anger tecknet som används för att kommentera rader med CSV-data.

```csharp
public char CommentChar { get; set; }
```

## Anmärkningar

Standardvärdet är '#' (nummertecken).

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
