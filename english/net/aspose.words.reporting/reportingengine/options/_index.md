---
title: ReportingEngine.Options
linktitle: Options
articleTitle: Options
second_title: Aspose.Words for .NET
description: ReportingEngine Options property. Gets or sets a set of flags controlling behavior of this ReportingEngine instance while building a report in C#.
type: docs
weight: 40
url: /net/aspose.words.reporting/reportingengine/options/
---
## ReportingEngine.Options property

Gets or sets a set of flags controlling behavior of this [`ReportingEngine`](../) instance while building a report.

```csharp
public ReportBuildOptions Options { get; set; }
```

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

* enum [ReportBuildOptions](../../reportbuildoptions/)
* class [ReportingEngine](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)
