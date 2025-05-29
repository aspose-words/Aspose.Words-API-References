---
title: XlsxDateTimeParsingMode Enum
linktitle: XlsxDateTimeParsingMode
articleTitle: XlsxDateTimeParsingMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية XlsxDateTimeParsingMode في Aspose.Words لتحليل نصوص المستندات بكفاءة. تعرّف بسهولة على قيم التاريخ والوقت في ملفاتك!
type: docs
weight: 6510
url: /ar/net/aspose.words.saving/xlsxdatetimeparsingmode/
---
## XlsxDateTimeParsingMode enumeration

يحدد كيفية تحليل نص المستند لتحديد قيم التاريخ والوقت.

```csharp
public enum XlsxDateTimeParsingMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| UseCurrentLocale | `0` | يُستخدم تنسيق التاريخ والوقت المُعيَّن للخيط الحالي أولًا لتحليل قيم السلسلة. إذا فشل التحليل، تُجرَّب تنسيقات تاريخ ووقت شائعة أخرى. |
| Auto | `1` | يتم تحديد تنسيق التاريخ والوقت المستخدم في المستند تلقائيًا. قد يستغرق هذا وقتًا إضافيًا. |

## أمثلة

يوضح كيفية تحديد الاكتشاف التلقائي لتنسيق التاريخ والوقت.

```csharp
Document doc = new Document(MyDir + "Xlsx DateTime.docx");

XlsxSaveOptions saveOptions = new XlsxSaveOptions();
// حدد باستخدام الكشف التلقائي عن تنسيق التاريخ والوقت.
saveOptions.DateTimeParsingMode = XlsxDateTimeParsingMode.Auto;

doc.Save(ArtifactsDir + "XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
