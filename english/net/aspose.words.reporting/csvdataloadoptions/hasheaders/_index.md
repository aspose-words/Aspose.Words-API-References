---
title: CsvDataLoadOptions.HasHeaders
linktitle: HasHeaders
articleTitle: HasHeaders
second_title: Aspose.Words for .NET
description: Discover CsvDataLoadOptions' HasHeaders property to easily manage CSV imports by specifying if the first record includes column names for seamless data integration.
type: docs
weight: 40
url: /net/aspose.words.reporting/csvdataloadoptions/hasheaders/
---
## CsvDataLoadOptions.HasHeaders property

Gets or sets a value indicating whether the first record of CSV data contains column names.

```csharp
public bool HasHeaders { get; set; }
```

## Remarks

The default value is `false`.

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
