---
title: FixedPageSaveOptions.NumeralFormat
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية NumeralFormat في FixedPageSaveOptions لتخصيص عرض الأرقام. انتقل بسهولة إلى الأرقام الأوروبية لعرض مُحسّن للمستندات.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/fixedpagesaveoptions/numeralformat/
---
## FixedPageSaveOptions.NumeralFormat property

يحصل أو يعين[`NumeralFormat`](../../numeralformat/) تُستخدم لعرض الأرقام. يتم استخدام الأرقام الأوروبية بشكل افتراضي.

```csharp
public NumeralFormat NumeralFormat { get; set; }
```

## ملاحظات

إذا تم تغيير قيمة هذه الخاصية وتم بناء تخطيط الصفحة بالفعل، فإن [`UpdatePageLayout`](../../../aspose.words/document/updatepagelayout/) يتم استدعاؤه تلقائيًا لتحديث أي تغييرات.

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

* enum [NumeralFormat](../../numeralformat/)
* class [FixedPageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
