---
title: FixedPageSaveOptions.NumeralFormat
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: Aspose.Words لـ .NET
description: FixedPageSaveOptions NumeralFormat ملكية. يحصل على أو مجموعاتNumeralFormat تستخدم لعرض الأرقام. يتم استخدام الأرقام الأوروبية بشكل افتراضي في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/fixedpagesaveoptions/numeralformat/
---
## FixedPageSaveOptions.NumeralFormat property

يحصل على أو مجموعات[`NumeralFormat`](../../numeralformat/) تستخدم لعرض الأرقام. يتم استخدام الأرقام الأوروبية بشكل افتراضي.

```csharp
public NumeralFormat NumeralFormat { get; set; }
```

## ملاحظات

إذا تم تغيير قيمة هذه الخاصية وتم إنشاء تخطيط الصفحة بالفعل، إذن [`UpdatePageLayout`](../../../aspose.words/document/updatepagelayout/) يتم استدعاؤه تلقائيًا لتحديث أي تغييرات.

## أمثلة

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

* enum [NumeralFormat](../../numeralformat/)
* class [FixedPageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
