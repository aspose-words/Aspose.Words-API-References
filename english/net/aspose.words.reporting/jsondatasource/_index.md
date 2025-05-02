---
title: JsonDataSource Class
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words for .NET
description: Unlock powerful reporting with Aspose.Words.Reporting.JsonDataSource. Easily access JSON data for seamless integration into your reports.
type: docs
weight: 5430
url: /net/aspose.words.reporting/jsondatasource/
---
## JsonDataSource class

Provides access to data of a JSON file or stream to be used within a report.

To learn more, visit the [LINQ Reporting Engine](https://docs.aspose.com/words/net/linq-reporting-engine/) documentation article.

```csharp
public class JsonDataSource
```

## Constructors

| Name | Description |
| --- | --- |
| [JsonDataSource](jsondatasource/#constructor)(*Stream*) | Creates a new data source with data from a JSON stream using default options for parsing JSON data. |
| [JsonDataSource](jsondatasource/#constructor_2)(*string*) | Creates a new data source with data from a JSON file using default options for parsing JSON data. |
| [JsonDataSource](jsondatasource/#constructor_1)(*Stream, [JsonDataLoadOptions](../jsondataloadoptions/)*) | Creates a new data source with data from a JSON stream using the specified options for parsing JSON data. |
| [JsonDataSource](jsondatasource/#constructor_3)(*string, [JsonDataLoadOptions](../jsondataloadoptions/)*) | Creates a new data source with data from a JSON file using the specified options for parsing JSON data. |

## Remarks

To access data of the corresponding file or stream while generating a report, pass an instance of this class as a data source to one of [`ReportingEngine`](../reportingengine/).BuildReport overloads.

In template documents, if a top-level JSON element is an array, a `JsonDataSource` instance should be treated in the same way as if it was a DataTable instance. If a top-level JSON element is an object, a `JsonDataSource` instance should be treated in the same way as if it was a DataRow instance. For more information, see template syntax reference (https://docs.aspose.com/display/wordsnet/Template+Syntax).

In template documents, you can work with typed values of JSON elements. For convenience, the engine replaces the set of JSON simple types with the following one:

* Nullable
* Nullable
* Nullable
* Nullable
* String

The engine automatically recognizes values of the extra types upon their JSON representations.

To override default behavior of JSON data loading, initialize and pass a [`JsonDataLoadOptions`](../jsondataloadoptions/) instance to a constructor of this class.

## Examples

Shows how to use JSON as a data source (string).

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

### See Also

* namespace [Aspose.Words.Reporting](../../aspose.words.reporting/)
* assembly [Aspose.Words](../../)
