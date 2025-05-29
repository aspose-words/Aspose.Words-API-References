---
title: XlsxSaveOptions.DateTimeParsingMode
linktitle: DateTimeParsingMode
articleTitle: DateTimeParsingMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية DateTimeParsingMode في XlsxSaveOptions لتخصيص كيفية تحليل مستندك للتواريخ والأوقات، مما يضمن تفسير البيانات بدقة.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/xlsxsaveoptions/datetimeparsingmode/
---
## XlsxSaveOptions.DateTimeParsingMode property

يحصل على الوضع الذي يحدد كيفية تحليل نص المستند لتحديد قيم التاريخ والوقت أو يعينه. القيمة الافتراضية هيUseCurrentLocale .

```csharp
public XlsxDateTimeParsingMode DateTimeParsingMode { get; set; }
```

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

* enum [XlsxDateTimeParsingMode](../../xlsxdatetimeparsingmode/)
* class [XlsxSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
