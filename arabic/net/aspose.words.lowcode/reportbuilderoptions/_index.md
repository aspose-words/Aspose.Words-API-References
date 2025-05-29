---
title: ReportBuilderOptions Class
linktitle: ReportBuilderOptions
articleTitle: ReportBuilderOptions
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words LowCode ReportBuilderOptions، المصممة لتعزيز تجربة LINQ Reporting Engine الخاصة بك مع خيارات قابلة للتخصيص لإنشاء مستندات سلسة.
type: docs
weight: 4380
url: /ar/net/aspose.words.lowcode/reportbuilderoptions/
---
## ReportBuilderOptions class

يمثل خيارات لوظيفة محرك التقارير LINQ.

```csharp
public class ReportBuilderOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [ReportBuilderOptions](reportbuilderoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [KnownTypes](../../aspose.words.lowcode/reportbuilderoptions/knowntypes/) { get; } | يحصل على مجموعة غير مرتبة (أي مجموعة من العناصر الفريدة) تحتوي علىType الكائنات التي يمكن استخدام أسمائها المؤهلة بالكامل أو جزئيًا داخل قوالب التقارير التي تتم معالجتها بواسطة مثيل engine هذا لاستدعاء الأعضاء الثابتة للأنواع المقابلة، وإجراء عمليات تحويل النوع، وما إلى ذلك. |
| [MissingMemberMessage](../../aspose.words.lowcode/reportbuilderoptions/missingmembermessage/) { get; set; } | يحصل على أو يعيّن قيمة سلسلة نصية مطبوعة بدلاً من تعبير قالب يمثل مرجعًا بسيطًا إلى ، وهو عنصر مفقود في كائن. القيمة الافتراضية هي سلسلة نصية فارغة. |
| [Options](../../aspose.words.lowcode/reportbuilderoptions/options/) { get; set; } | يحصل على مجموعة من العلامات التي تتحكم في سلوك هذا أو يعينها[`ReportingEngine`](../../aspose.words.reporting/reportingengine/) مثال أثناء بناء تقرير. |

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

* مساحة الاسم [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../)
