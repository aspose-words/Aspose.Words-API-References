---
title: JsonDataLoadOptions Class
linktitle: JsonDataLoadOptions
articleTitle: JsonDataLoadOptions
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Reporting.JsonDataLoadOptions class for seamless JSON data parsing. Enhance your document processing with flexible options!
type: docs
weight: 5450
url: /net/aspose.words.reporting/jsondataloadoptions/
---
## JsonDataLoadOptions class

Represents options for parsing JSON data.

To learn more, visit the [LINQ Reporting Engine](https://docs.aspose.com/words/net/linq-reporting-engine/) documentation article.

```csharp
public class JsonDataLoadOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [JsonDataLoadOptions](jsondataloadoptions/)() | Initializes a new instance of this class with default options. |

## Properties

| Name | Description |
| --- | --- |
| [AlwaysGenerateRootObject](../../aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/) { get; set; } | Gets or sets a flag indicating whether a generated data source will always contain an object for a JSON root element. If a JSON root element contains a single complex property, such an object is not created by default. |
| [ExactDateTimeParseFormats](../../aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/) { get; set; } | Gets or sets exact formats for parsing JSON date-time values while loading JSON. The default is `null`. |
| [PreserveSpaces](../../aspose.words.reporting/jsondataloadoptions/preservespaces/) { get; set; } | Gets or sets a flag indicating whether leading and trailing spaces should be preserved when loading string values of JSON data. |
| [SimpleValueParseMode](../../aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/) { get; set; } | Gets or sets a mode for parsing JSON simple values (null, boolean, number, integer, and string) while loading JSON. Such a mode does not affect parsing of date-time values. The default is Loose. |

## Remarks

An instance of this class can be passed into constructors of [`JsonDataSource`](../jsondatasource/).

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
