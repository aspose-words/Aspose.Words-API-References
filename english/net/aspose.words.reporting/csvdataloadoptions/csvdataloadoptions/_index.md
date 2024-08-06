---
title: CsvDataLoadOptions
linktitle: CsvDataLoadOptions
articleTitle: CsvDataLoadOptions
second_title: Aspose.Words for .NET
description: CsvDataLoadOptions constructor. Initializes a new instance of this class with default options in C#.
type: docs
weight: 10
url: /net/aspose.words.reporting/csvdataloadoptions/csvdataloadoptions/
---
## CsvDataLoadOptions() {#constructor}

Initializes a new instance of this class with default options.

```csharp
public CsvDataLoadOptions()
```

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

---

## CsvDataLoadOptions(*bool*) {#constructor_1}

Initializes a new instance of this class with specifying whether CSV data contains column names at the first line.

```csharp
public CsvDataLoadOptions(bool hasHeaders)
```

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
