---
title: CsvDataSource
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words for .NET
description: CsvDataSource constructor. Creates a new data source with data from a CSV file using default options for parsing CSV data in C#.
type: docs
weight: 10
url: /net/aspose.words.reporting/csvdatasource/csvdatasource/
---
## CsvDataSource(*string*) {#constructor_2}

Creates a new data source with data from a CSV file using default options for parsing CSV data.

```csharp
public CsvDataSource(string csvPath)
```

| Parameter | Type | Description |
| --- | --- | --- |
| csvPath | String | The path to the CSV file to be used as the data source. |

### See Also

* class [CsvDataSource](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)

---

## CsvDataSource(*string, [CsvDataLoadOptions](../../csvdataloadoptions/)*) {#constructor_3}

Creates a new data source with data from a CSV file using the specified options for parsing CSV data.

```csharp
public CsvDataSource(string csvPath, CsvDataLoadOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| csvPath | String | The path to the CSV file to be used as the data source. |
| options | CsvDataLoadOptions | Options for parsing the CSV data. |

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

* class [CsvDataLoadOptions](../../csvdataloadoptions/)
* class [CsvDataSource](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)

---

## CsvDataSource(*Stream*) {#constructor}

Creates a new data source with data from a CSV stream using default options for parsing CSV data.

```csharp
public CsvDataSource(Stream csvStream)
```

| Parameter | Type | Description |
| --- | --- | --- |
| csvStream | Stream | The stream of CSV data to be used as the data source. |

### See Also

* class [CsvDataSource](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)

---

## CsvDataSource(*Stream, [CsvDataLoadOptions](../../csvdataloadoptions/)*) {#constructor_1}

Creates a new data source with data from a CSV stream using the specified options for parsing CSV data.

```csharp
public CsvDataSource(Stream csvStream, CsvDataLoadOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| csvStream | Stream | The stream of CSV data to be used as the data source. |
| options | CsvDataLoadOptions | Options for parsing the CSV data. |

## Examples

Shows how to use CSV as a data source (stream).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - CSV data destination.docx");

CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
loadOptions.Delimiter = ';';
loadOptions.CommentChar = '$';

using (FileStream stream = File.OpenRead(MyDir + "List of people.csv"))
{
    CsvDataSource dataSource = new CsvDataSource(stream, loadOptions);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.CsvDataStream.docx");
```

### See Also

* class [CsvDataLoadOptions](../../csvdataloadoptions/)
* class [CsvDataSource](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)
