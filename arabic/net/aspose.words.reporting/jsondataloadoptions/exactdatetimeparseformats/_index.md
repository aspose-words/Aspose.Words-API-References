---
title: JsonDataLoadOptions.ExactDateTimeParseFormats
linktitle: ExactDateTimeParseFormats
articleTitle: ExactDateTimeParseFormats
second_title: Aspose.Words لـ .NET
description: JsonDataLoadOptions ExactDateTimeParseFormats ملكية. الحصول على التنسيقات الدقيقة أو تعيينها لتحليل قيم وقت التاريخ JSON أثناء تحميل JSON. الافتراضي هوباطل  في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/
---
## JsonDataLoadOptions.ExactDateTimeParseFormats property

الحصول على التنسيقات الدقيقة أو تعيينها لتحليل قيم وقت التاريخ JSON أثناء تحميل JSON. الافتراضي هو`باطل` .

```csharp
public IEnumerable<string> ExactDateTimeParseFormats { get; set; }
```

## ملاحظات

السلاسل المشفرة باستخدام تنسيق التاريخ والوقت Microsoft® JSON (على سبيل المثال، "/Date(1224043200000)/") يتم التعرف عليها دائمًا كقيم وقت وتاريخ بغض النظر عن قيمة هذه الخاصية. تحدد الخاصية تنسيقات إضافية لاستخدامها أثناء تحليل قيم التاريخ والوقت من السلاسل بالطريقة التالية:

* متى`ExactDateTimeParseFormats` يكون`باطل`، يتم استخدام تنسيق ISO-8601 وجميع تنسيقات التاريخ والوقت المدعومة للثقافات الحالية والإنجليزية الأمريكية والإنجليزية النيوزيلندية بشكل إضافي في بالترتيب المذكور.
* متى`ExactDateTimeParseFormats` تحتوي على سلاسل، يتم استخدامها كتنسيقات date-time إضافية باستخدام الثقافة الحالية.
* متى`ExactDateTimeParseFormats` فارغ، ولم يتم استخدام أي تنسيقات وقت وتاريخ إضافية.

### أنظر أيضا

* class [JsonDataLoadOptions](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)
