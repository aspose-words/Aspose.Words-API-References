---
title: CsvDataLoadOptions.QuoteChar
linktitle: QuoteChar
articleTitle: QuoteChar
second_title: Aspose.Words for .NET
description: Discover the CsvDataLoadOptions QuoteChar property to easily customize field value quoting for seamless data handling and improved CSV management.
type: docs
weight: 50
url: /net/aspose.words.reporting/csvdataloadoptions/quotechar/
---
## CsvDataLoadOptions.QuoteChar property

Gets or sets the character that is used to quote field values.

```csharp
public char QuoteChar { get; set; }
```

## Remarks

The default value is '"' (quotation mark).

Double the character to place it into quoted text.

## Examples

Shows how to use CSV as a data source (string).

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

### See Also

* class [CsvDataLoadOptions](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)
