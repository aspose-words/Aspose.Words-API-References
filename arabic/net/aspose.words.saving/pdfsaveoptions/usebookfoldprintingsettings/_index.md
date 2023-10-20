---
title: PdfSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words لـ .NET
description: PdfSaveOptions UseBookFoldPrintingSettings ملكية. الحصول على قيمة منطقية أو تعيينها تشير إلى ما إذا كان يجب حفظ المستند باستخدام تخطيط طباعة الكتيبات إذا تم تحديده عبرMultiplePages  في C#.
type: docs
weight: 300
url: /ar/net/aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/
---
## PdfSaveOptions.UseBookFoldPrintingSettings property

الحصول على قيمة منطقية أو تعيينها تشير إلى ما إذا كان يجب حفظ المستند باستخدام تخطيط طباعة الكتيبات، إذا تم تحديده عبر[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## ملاحظات

إذا تم تحديد هذا الخيار،[`PageSet`](../../fixedpagesaveoptions/pageset/) يتم تجاهله عند الحفظ. يتطابق هذا السلوك مع MS Word. إذا لم يتم تحديد إعدادات طباعة طي الكتاب في إعداد الصفحة، فلن يكون لهذا الخيار أي تأثير.

## أمثلة

يوضح كيفية حفظ مستند بتنسيق PDF على شكل طية كتاب.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "UseBookFoldPrintingSettings" على "صحيح" لترتيب المحتويات
// في ملف PDF الناتج بطريقة تساعدنا على استخدامه لعمل كتيب.
// اضبط خاصية "UseBookFoldPrintingSettings" على "خطأ" لعرض ملف PDF بشكل طبيعي.
options.UseBookFoldPrintingSettings = renderTextAsBookfold;

// إذا كنا نعرض المستند ككتيب، فيجب علينا تعيين "الصفحات المتعددة"
// خصائص كائنات إعداد الصفحة لجميع الأقسام إلى "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookfold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// بمجرد طباعة هذه الوثيقة على جانبي الصفحات، يمكننا طي جميع الصفحات إلى المنتصف مرة واحدة،
// وسوف تصطف المحتويات بطريقة تُنشئ كتيبًا.
doc.Save(ArtifactsDir + "PdfSaveOptions.SaveAsPdfBookFold.pdf", options);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
