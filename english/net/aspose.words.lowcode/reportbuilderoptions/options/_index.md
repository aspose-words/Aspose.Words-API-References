---
title: ReportBuilderOptions.Options
linktitle: Options
articleTitle: Options
second_title: Aspose.Words for .NET
description: Discover the ReportBuilderOptions property to customize your ReportingEngine's behavior, enhancing report creation with flexible control and improved functionality.
type: docs
weight: 40
url: /net/aspose.words.lowcode/reportbuilderoptions/options/
---
## ReportBuilderOptions.Options property

Gets or sets a set of flags controlling behavior of this [`ReportingEngine`](../../../aspose.words.reporting/reportingengine/) instance while building a report.

```csharp
public ReportBuildOptions Options { get; set; }
```

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

* enum [ReportBuildOptions](../../../aspose.words.reporting/reportbuildoptions/)
* class [ReportBuilderOptions](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
