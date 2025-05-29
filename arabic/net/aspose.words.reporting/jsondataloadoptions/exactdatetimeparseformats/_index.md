---
title: JsonDataLoadOptions.ExactDateTimeParseFormats
linktitle: ExactDateTimeParseFormats
articleTitle: ExactDateTimeParseFormats
second_title: Aspose.Words لـ .NET
description: اكتشف تنسيقات ExactDateTimeParseFormats في JsonDataLoadOptions لتحليل دقيق لبيانات JSON. خصّص التنسيقات بسهولة لتحميل البيانات بسلاسة!
type: docs
weight: 30
url: /ar/net/aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/
---
## JsonDataLoadOptions.ExactDateTimeParseFormats property

يحصل على أو يضبط التنسيقات الدقيقة لتحليل قيم التاريخ والوقت JSON أثناء تحميل JSON. الإعداد الافتراضي هو`باطل` .

```csharp
public IEnumerable<string> ExactDateTimeParseFormats { get; set; }
```

## ملاحظات

السلاسل النصية المُرمَّزة باستخدام تنسيق التاريخ والوقت Microsoft® JSON (على سبيل المثال، "/Date(1224043200000)/") تُعرَّف دائمًا على أنها قيم تاريخ ووقت باستخدام بغض النظر عن قيمة هذه الخاصية. تُحدِّد هذه الخاصية تنسيقات إضافية لاستخدامها أثناء تحليل قيم التاريخ والوقت من السلاسل النصية بالطريقة التالية:

* عندما`ExactDateTimeParseFormats` يكون`باطل` يتم استخدام تنسيق ISO-8601 وجميع تنسيقات التاريخ والوقت المدعومة للثقافات الحالية، الإنجليزية الأمريكية، والإنجليزية النيوزيلندية، بالإضافة إلى ذلك في بالترتيب المذكور.
* عندما`ExactDateTimeParseFormats`تحتوي على سلاسل، يتم استخدامها كتنسيقات إضافية للتاريخ والوقت باستخدام الثقافة الحالية.
* عندما`ExactDateTimeParseFormats` فارغ، لا يتم استخدام تنسيقات إضافية للتاريخ والوقت.

## أمثلة

يوضح كيفية استخدام JSON كمصدر بيانات (سلسلة).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - JSON data destination.docx");

JsonDataLoadOptions options = new JsonDataLoadOptions
{
    ExactDateTimeParseFormats = new List<string> {"MM/dd/yyyy", "MM.d.yy", "MM d yy"},
    AlwaysGenerateRootObject = true,
    PreserveSpaces = true,
    SimpleValueParseMode = JsonSimpleValueParseMode.Loose
};

JsonDataSource dataSource = new JsonDataSource(MyDir + "List of people.json", options);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.JsonDataString.docx");
```

### أنظر أيضا

* class [JsonDataLoadOptions](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)
