---
title: ReportBuilderOptions Class
linktitle: ReportBuilderOptions
articleTitle: ReportBuilderOptions
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words LowCode ReportBuilderOptions class, designed to enhance your LINQ Reporting Engine experience with customizable options for seamless document generation.
type: docs
weight: 4400
url: /net/aspose.words.lowcode/reportbuilderoptions/
---
## ReportBuilderOptions class

Represents options for the LINQ Reporting Engine functionality.

```csharp
public class ReportBuilderOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [ReportBuilderOptions](reportbuilderoptions/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [KnownTypes](../../aspose.words.lowcode/reportbuilderoptions/knowntypes/) { get; } | Gets an unordered set (i.e. a collection of unique items) containing Type objects which fully or partially qualified names can be used within report templates processed by this engine instance to invoke the corresponding types' static members, perform type casts, etc. |
| [MissingMemberMessage](../../aspose.words.lowcode/reportbuilderoptions/missingmembermessage/) { get; set; } | Gets or sets a string value printed instead of a template expression that represents a plain reference to a missing member of an object. The default value is an empty string. |
| [Options](../../aspose.words.lowcode/reportbuilderoptions/options/) { get; set; } | Gets or sets a set of flags controlling behavior of this [`ReportingEngine`](../../aspose.words.reporting/reportingengine/) instance while building a report. |

## Examples

Shows how to populate document with data.

```csharp
public void BuildReportData()
{
    // There is a several ways to populate document with data:
    string doc = MyDir + "Reporting engine template - If greedy.docx";

    AsposeData obj = new AsposeData { List = new List<string> { "abc" } };

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.1.docx", obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.2.docx", obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.3.docx", SaveFormat.Docx, obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.4.docx", SaveFormat.Docx, obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
}

public class AsposeData
{
    public List<string> List { get; set; }
}
```

### See Also

* namespace [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../)
