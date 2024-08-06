---
title: ReportingEngine.MissingMemberMessage
linktitle: MissingMemberMessage
articleTitle: MissingMemberMessage
second_title: Aspose.Words for .NET
description: ReportingEngine MissingMemberMessage property. Gets or sets a string value printed instead of a template expression that represents a plain reference to a missing member of an object. The default value is an empty string in C#.
type: docs
weight: 30
url: /net/aspose.words.reporting/reportingengine/missingmembermessage/
---
## ReportingEngine.MissingMemberMessage property

Gets or sets a string value printed instead of a template expression that represents a plain reference to a missing member of an object. The default value is an empty string.

```csharp
public string MissingMemberMessage { get; set; }
```

## Remarks

The property should be used in conjunction with the AllowMissingMembers option. Otherwise, an exception is thrown when a missing member of an object is encountered.

The property affects only printing of a template expression representing a plain reference to a missing object member. For example, printing of a binary operator, one of which operands references a missing object member, is not affected.

The value of this property cannot be set to null.

## Examples

Shows how to allow missinng members.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

### See Also

* class [ReportingEngine](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)
