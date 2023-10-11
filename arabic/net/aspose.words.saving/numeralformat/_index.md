---
title: Enum NumeralFormat
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.NumeralFormat تعداد. يشير إلى مجموعة الرموز المستخدمة لتمثيل أرقام أثناء العرض إلى تنسيقات الصفحات الثابتة.
type: docs
weight: 5310
url: /ar/net/aspose.words.saving/numeralformat/
---
## NumeralFormat enumeration

يشير إلى مجموعة الرموز المستخدمة لتمثيل أرقام أثناء العرض إلى تنسيقات الصفحات الثابتة.

```csharp
public enum NumeralFormat
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| European | `0` | الأرقام الأوروبية : 0123456789. |
| ArabicIndic | `1` | الأرقام المستخدمة في اللغة العربية: ٠١٢٣٤٥٦٧٨٩. نطاق Unicode U+0660 - u+0669. |
| EasternArabicIndic | `2` | الأرقام المستخدمة باللغتين الفارسية والأردية: ۰۱۲۳۴۵۶۷۸٩. نطاق Unicode U+06F0 - u+06F9. |
| Context | `3` | يتم تحديد مجموعة الرموز من السياق (اللغة المحلية وخاصية RTL). |
| System | `4` | هذا الخيار غير مدعوم. يتم تحديد مجموعة الرموز من الإعدادات الإقليمية. |

### أمثلة

يوضح كيفية ضبط التنسيق الرقمي المستخدم عند الحفظ إلى PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.LocaleId = new CultureInfo("ar-AR").LCID;
builder.Writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "NumeralFormat" على "NumeralFormat.ArabicIndic" إلى
// استخدم الحروف الرسومية من نطاق U+0660 إلى U+0669 كأرقام.
// قم بتعيين خاصية "NumeralFormat" على "NumeralFormat.Context" إلى
// ابحث عن اللغة لتحديد عدد الحروف الرسومية التي سيتم استخدامها.
// اضبط خاصية "NumeralFormat" على "NumeralFormat.EasternArabicIndic" إلى
// استخدم الحروف الرسومية من نطاق U+06F0 إلى U+06F9 كأرقام.
// اضبط خاصية "NumeralFormat" على "NumeralFormat.European" لاستخدام الأرقام الأوروبية.
// قم بتعيين خاصية "NumeralFormat" على "NumeralFormat.System" لتحديد مجموعة الرموز من الإعدادات الإقليمية.
options.NumeralFormat = numeralFormat;

doc.Save(ArtifactsDir + "PdfSaveOptions.SetNumeralFormat.pdf", options);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


