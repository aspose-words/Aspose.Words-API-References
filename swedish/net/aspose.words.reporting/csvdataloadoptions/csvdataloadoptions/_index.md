---
title: CsvDataLoadOptions
linktitle: CsvDataLoadOptions
articleTitle: CsvDataLoadOptions
second_title: Aspose.Words för .NET
description: Upptäck CsvDataLoadOptions-konstruktorn – initiera enkelt med standardinställningar för effektiv datainläsning och sömlös integration.
type: docs
weight: 10
url: /sv/net/aspose.words.reporting/csvdataloadoptions/csvdataloadoptions/
---
## CsvDataLoadOptions() {#constructor}

Initierar en ny instans av den här klassen med standardalternativ.

```csharp
public CsvDataLoadOptions()
```

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

---

## CsvDataLoadOptions(*bool*) {#constructor_1}

Initierar en ny instans av denna klass genom att ange om CSV-data innehåller kolumnnamnen på första raden.

```csharp
public CsvDataLoadOptions(bool hasHeaders)
```

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
