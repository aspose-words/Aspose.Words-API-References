---
title: JsonSimpleValueParseMode Enum
linktitle: JsonSimpleValueParseMode
articleTitle: JsonSimpleValueParseMode
second_title: Aspose.Words for .NET
description: Aspose.Words.Reporting.JsonSimpleValueParseMode enum. Specifies a mode for parsing JSON simple values null boolean number integer and string while loading JSON. Such a mode does not affect parsing of datetime values in C#.
type: docs
weight: 4860
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

### See Also

* namespace [Aspose.Words.Reporting](../../aspose.words.reporting/)
* assembly [Aspose.Words](../../)
