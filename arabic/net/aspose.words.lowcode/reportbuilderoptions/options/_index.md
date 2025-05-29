---
title: ReportBuilderOptions.Options
linktitle: Options
articleTitle: Options
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ReportBuilderOptions لتخصيص سلوك ReportingEngine الخاص بك، وتحسين إنشاء التقارير باستخدام التحكم المرن والوظائف المحسنة.
type: docs
weight: 40
url: /ar/net/aspose.words.lowcode/reportbuilderoptions/options/
---
## ReportBuilderOptions.Options property

يحصل على مجموعة من العلامات التي تتحكم في سلوك هذا أو يعينها[`ReportingEngine`](../../../aspose.words.reporting/reportingengine/) مثال أثناء بناء تقرير.

```csharp
public ReportBuildOptions Options { get; set; }
```

## أمثلة

يوضح كيفية ملء المستند بالبيانات.

```csharp
public void BuildReportData()
{
    // هناك عدة طرق لملء المستند بالبيانات:
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

### أنظر أيضا

* enum [ReportBuildOptions](../../../aspose.words.reporting/reportbuildoptions/)
* class [ReportBuilderOptions](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
