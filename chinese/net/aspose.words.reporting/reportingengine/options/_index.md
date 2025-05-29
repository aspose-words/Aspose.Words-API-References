---
title: ReportingEngine.Options
linktitle: Options
articleTitle: Options
second_title: Aspose.Words for .NET
description: 发现 ReportingEngine 选项属性，使用灵活的标志轻松定制报告构建行为，以实现最佳性能和控制。
type: docs
weight: 40
url: /zh/net/aspose.words.reporting/reportingengine/options/
---
## ReportingEngine.Options property

获取或设置一组控制此行为的标志[`ReportingEngine`](../)实例 ，同时构建报告。

```csharp
public ReportBuildOptions Options { get; set; }
```

## 例子

展示如何允许缺少成员。

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

### 也可以看看

* enum [ReportBuildOptions](../../reportbuildoptions/)
* class [ReportingEngine](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)
