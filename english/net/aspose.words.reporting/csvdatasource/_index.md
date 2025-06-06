---
title: CsvDataSource Class
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words for .NET
description: Access and utilize CSV data effortlessly with Aspose.Words.Reporting.CsvDataSource. Enhance your reports with seamless data integration!
type: docs
weight: 5410
url: /net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

Provides access to data of a CSV file or stream to be used within a report.

To learn more, visit the [LINQ Reporting Engine](https://docs.aspose.com/words/net/linq-reporting-engine/) documentation article.

```csharp
public class CsvDataSource
```

## Constructors

| Name | Description |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(*Stream*) | Creates a new data source with data from a CSV stream using default options for parsing CSV data. |
| [CsvDataSource](csvdatasource/#constructor_2)(*string*) | Creates a new data source with data from a CSV file using default options for parsing CSV data. |
| [CsvDataSource](csvdatasource/#constructor_1)(*Stream, [CsvDataLoadOptions](../csvdataloadoptions/)*) | Creates a new data source with data from a CSV stream using the specified options for parsing CSV data. |
| [CsvDataSource](csvdatasource/#constructor_3)(*string, [CsvDataLoadOptions](../csvdataloadoptions/)*) | Creates a new data source with data from a CSV file using the specified options for parsing CSV data. |

## Remarks

To access data of the corresponding file or stream while generating a report, pass an instance of this class as a data source to one of [`ReportingEngine`](../reportingengine/).BuildReport overloads.

In template documents, a `CsvDataSource` instance should be treated in the same way as if it was a DataTable instance. For more information, see template syntax reference (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Data types of comma-separated values are determined automatically upon their string representations. So in template documents, you can work with typed values rather than just strings. The engine is capable to automatically recognize values of the following types:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Note that for automatic recognition of data types to work, string representations of comma-separated values should be formed using invariant culture settings.

To override default behavior of CSV data loading, initialize and pass a [`CsvDataLoadOptions`](../csvdataloadoptions/) instance to a constructor of this class.

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

* namespace [Aspose.Words.Reporting](../../aspose.words.reporting/)
* assembly [Aspose.Words](../../)
