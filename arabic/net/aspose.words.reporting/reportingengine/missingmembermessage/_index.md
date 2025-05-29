---
title: ReportingEngine.MissingMemberMessage
linktitle: MissingMemberMessage
articleTitle: MissingMemberMessage
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية MissingMemberMessage في ReportingEngine، وخصّص الرسائل لأعضاء الكائن المفقودين بسهولة. حسّن تجربة المستخدم بسهولة!
type: docs
weight: 30
url: /ar/net/aspose.words.reporting/reportingengine/missingmembermessage/
---
## ReportingEngine.MissingMemberMessage property

يحصل على أو يعيّن قيمة سلسلة نصية مطبوعة بدلاً من تعبير قالب يمثل مرجعًا بسيطًا إلى ، وهو عنصر مفقود في كائن. القيمة الافتراضية هي سلسلة نصية فارغة.

```csharp
public string MissingMemberMessage { get; set; }
```

## ملاحظات

يجب استخدام الخاصية بالتزامن معAllowMissingMembers خيار . وإلا، فسيتم طرح استثناء عند العثور على عنصر مفقود من الكائن.

تؤثر الخاصية فقط على طباعة تعبير قالب يمثل مرجعًا بسيطًا لعنصر كائن missing . على سبيل المثال، لا تتأثر طباعة عامل ثنائي، حيث تشير إحدى معاملاته إلى عنصر كائن missing .

لا يمكن تعيين قيمة هذه الخاصية إلى null.

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

* class [ReportingEngine](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)
