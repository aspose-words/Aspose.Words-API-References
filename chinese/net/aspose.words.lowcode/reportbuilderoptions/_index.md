---
title: ReportBuilderOptions Class
linktitle: ReportBuilderOptions
articleTitle: ReportBuilderOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words LowCode ReportBuilderOptions 类，旨在通过可自定义的选项增强您的 LINQ 报告引擎体验，实现无缝文档生成。
type: docs
weight: 4380
url: /zh/net/aspose.words.lowcode/reportbuilderoptions/
---
## ReportBuilderOptions class

表示 LINQ 报告引擎功能的选项。

```csharp
public class ReportBuilderOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [ReportBuilderOptions](reportbuilderoptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [KnownTypes](../../aspose.words.lowcode/reportbuilderoptions/knowntypes/) { get; } | 获取包含以下项的无序集合（即唯一项的集合）Type对象 的完全或部分限定名称可在由此引擎 实例处理的报告模板中使用，以调用相应类型的静态成员、执行类型转换等。 |
| [MissingMemberMessage](../../aspose.words.lowcode/reportbuilderoptions/missingmembermessage/) { get; set; } | 获取或设置打印的字符串值，而不是模板表达式，该值表示对对象缺失成员的简单引用。默认值为空字符串。 |
| [Options](../../aspose.words.lowcode/reportbuilderoptions/options/) { get; set; } | 获取或设置一组控制此行为的标志[`ReportingEngine`](../../aspose.words.reporting/reportingengine/)实例 ，同时构建报告。 |

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

* 命名空间 [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../)
