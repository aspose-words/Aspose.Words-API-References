---
title: NumeralFormat Enum
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Saving.NumeralFormat enum لتمثيل الأرقام بشكل مثالي في تنسيقات الصفحات الثابتة. حسّن عرض مستنداتك اليوم!
type: docs
weight: 6090
url: /ar/net/aspose.words.saving/numeralformat/
---
## NumeralFormat enumeration

يشير إلى مجموعة الرموز المستخدمة لتمثيل الأرقام أثناء العرض إلى تنسيقات الصفحة الثابتة.

```csharp
public enum NumeralFormat
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| European | `0` | الأرقام الأوروبية: 0123456789. |
| ArabicIndic | `1` | الأرقام المستخدمة في اللغة العربية: ٠١٢٣٤٥٦٧٨٩. نطاق Unicode U+0660 - u+0669. |
| EasternArabicIndic | `2` | الأرقام المستخدمة في الفارسية والأردية: 0123456789. نطاق Unicode U+06F0 - u+06F9. |
| Context | `3` | يتم تحديد مجموعة الرموز من السياق (الإعدادات المحلية وخاصية RTL). |
| System | `4` | هذا الخيار غير مدعوم. يتم تحديد مجموعة الرموز من الإعدادات الإقليمية. |

## أمثلة

يوضح كيفية تعيين تنسيق الأرقام المستخدم عند الحفظ بتنسيق PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.LocaleId = new CultureInfo("ar-AR").LCID;
builder.Writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "NumeralFormat" إلى "NumeralFormat.EnglishIndic"
// استخدم الحروف من النطاق U+0660 إلى U+0669 كأرقام.
// قم بتعيين خاصية "NumeralFormat" إلى "NumeralFormat.Context" لـ
// ابحث عن الإعدادات المحلية لتحديد عدد الحروف الرسومية التي يجب استخدامها.
// اضبط خاصية "NumeralFormat" إلى "NumeralFormat.EasternEnglishIndic"
// استخدم الحروف من النطاق U+06F0 إلى U+06F9 كأرقام.
// قم بتعيين خاصية "NumeralFormat" إلى "NumeralFormat.European" لاستخدام الأرقام الأوروبية.
// قم بتعيين خاصية "NumeralFormat" إلى "NumeralFormat.System" لتحديد مجموعة الرموز من الإعدادات الإقليمية.
options.NumeralFormat = numeralFormat;

doc.Save(ArtifactsDir + "PdfSaveOptions.SetNumeralFormat.pdf", options);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
