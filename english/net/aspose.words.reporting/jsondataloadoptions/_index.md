---
title: JsonDataLoadOptions Class
linktitle: JsonDataLoadOptions
articleTitle: JsonDataLoadOptions
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Reporting.JsonDataLoadOptions class. Represents options for parsing JSON data in C#.
type: docs
weight: 4590
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
| [SimpleValueParseMode](../../aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/) { get; set; } | Gets or sets a mode for parsing JSON simple values (null, boolean, number, integer, and string) while loading JSON. Such a mode does not affect parsing of date-time values. The default is Loose. |

## Remarks

An instance of this class can be passed into constructors of [`JsonDataSource`](../jsondatasource/).

### See Also

* namespace [Aspose.Words.Reporting](../../aspose.words.reporting/)
* assembly [Aspose.Words](../../)
