---
title: ReportingEngine.Options
linktitle: Options
articleTitle: Options
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية خيارات ReportingEngine لتخصيص سلوكيات بناء التقارير بسهولة باستخدام علامات مرنة لتحقيق الأداء والتحكم الأمثل.
type: docs
weight: 40
url: /ar/net/aspose.words.reporting/reportingengine/options/
---
## ReportingEngine.Options property

يحصل على مجموعة من العلامات التي تتحكم في سلوك هذا أو يعينها[`ReportingEngine`](../) مثال أثناء بناء تقرير.

```csharp
public ReportBuildOptions Options { get; set; }
```

## أمثلة

يوضح كيفية السماح للأعضاء المفقودين.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

### أنظر أيضا

* enum [ReportBuildOptions](../../reportbuildoptions/)
* class [ReportingEngine](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)
