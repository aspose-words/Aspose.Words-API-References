---
title: Enum NumeralFormat
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.NumeralFormat تعداد. يشير إلى مجموعة الرموز المستخدمة لتمثيل number أثناء التقديم إلى تنسيقات الصفحة الثابتة.
type: docs
weight: 5030
url: /ar/net/aspose.words.saving/numeralformat/
---
## NumeralFormat enumeration

يشير إلى مجموعة الرموز المستخدمة لتمثيل number أثناء التقديم إلى تنسيقات الصفحة الثابتة.

```csharp
public enum NumeralFormat
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| European | `0` | الأرقام الأوروبية: 0123456789. |
| ArabicIndic | `1` | الأرقام المستخدمة باللغة العربية: ٠١٢٣٤٥٦٧٨٩. نطاق Unicode U + 0660 - u + 0669. |
| EasternArabicIndic | `2` | الأرقام المستخدمة بالفارسية والأردية: ۰۱۲۳۴۵۶۷۸۹. نطاق Unicode U + 06F0 - u + 06F9. |
| Context | `3` | تم تحديد مجموعة الرموز من السياق (الخاصية المحلية وخاصية RTL) . |
| System | `4` | هذا الخيار غير معتمد. تم تحديد مجموعة الرموز من الإعدادات الإقليمية. |

### أمثلة

يوضح كيفية ضبط تنسيق الأرقام المستخدم عند الحفظ في PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.LocaleId = new CultureInfo("ar-AR").LCID;
builder.Writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
PdfSaveOptions options = new PdfSaveOptions();

// تعيين خاصية "NumeralFormat" إلى "NumeralFormat.ArabicIndic" إلى
// استخدم الحروف الرسومية من النطاق U + 0660 إلى U + 0669 كأرقام.
// قم بتعيين الخاصية "NumeralFormat" على "NumeralFormat.Context" إلى
// ابحث عن الإعدادات المحلية لتحديد عدد الحروف الرسومية المراد استخدامها.
// تعيين خاصية "NumeralFormat" إلى "NumeralFormat.EasternArabicIndic" إلى
// استخدم الحروف الرسومية من النطاق U + 06F0 إلى U + 06F9 كأرقام.
// اضبط خاصية "NumeralFormat" على "NumeralFormat.European" لاستخدام الأرقام الأوروبية.
// اضبط خاصية "NumeralFormat" على "NumeralFormat.System" لتحديد مجموعة الرموز من الإعدادات الإقليمية.
options.NumeralFormat = numeralFormat;

doc.Save(ArtifactsDir + "PdfSaveOptions.SetNumeralFormat.pdf", options);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


