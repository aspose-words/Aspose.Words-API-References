---
title: JsonSimpleValueParseMode Enum
linktitle: JsonSimpleValueParseMode
articleTitle: JsonSimpleValueParseMode
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Reporting.JsonSimpleValueParseMode enum for efficient JSON parsing. Easily handle nulls, booleans, numbers, and strings seamlessly!
type: docs
weight: 5490
url: /net/aspose.words.reporting/jsonsimplevalueparsemode/
---
## JsonSimpleValueParseMode enumeration

Specifies a mode for parsing JSON simple values (null, boolean, number, integer, and string) while loading JSON. Such a mode does not affect parsing of date-time values.

```csharp
public enum JsonSimpleValueParseMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Loose | `0` | Specifies the mode where types of JSON simple values are determined upon parsing of their string representations. For example, the type of 'prop' from the JSON snippet '{ prop: "123" }' is determined as integer in this mode. |
| Strict | `1` | Specifies the mode where types of JSON simple values are determined from JSON notation itself. For example, the type of 'prop' from the JSON snippet '{ prop: "123" }' is determined as string in this mode. |

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
