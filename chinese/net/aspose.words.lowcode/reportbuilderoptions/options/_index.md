---
title: ReportBuilderOptions.Options
linktitle: Options
articleTitle: Options
second_title: Aspose.Words for .NET
description: 发现 ReportBuilderOptions 属性来定制 ReportingEngine 的行为，通过灵活的控制和改进的功能增强报告创建。
type: docs
weight: 40
url: /zh/net/aspose.words.lowcode/reportbuilderoptions/options/
---
## ReportBuilderOptions.Options property

获取或设置一组控制此行为的标志[`ReportingEngine`](../../../aspose.words.reporting/reportingengine/)实例 ，同时构建报告。

```csharp
public ReportBuildOptions Options { get; set; }
```

## 例子

展示如何用数据填充文档。

```csharp
public void BuildReportData()
{
    // 有几种方法可以用数据填充文档：
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

### 也可以看看

* enum [ReportBuildOptions](../../../aspose.words.reporting/reportbuildoptions/)
* class [ReportBuilderOptions](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
