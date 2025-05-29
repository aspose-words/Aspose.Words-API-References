---
title: PdfSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PdfSaveOptions UseBookFoldPrintingSettings لحفظ المستندات بسهولة في تخطيط كتيب لتحسين كفاءة الطباعة.
type: docs
weight: 320
url: /ar/net/aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/
---
## PdfSaveOptions.UseBookFoldPrintingSettings property

يحصل على قيمة منطقية أو يعينها للإشارة إلى ما إذا كان يجب حفظ المستند باستخدام تخطيط طباعة الكتيبات، إذا تم تحديد ذلك عبر[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## ملاحظات

إذا تم تحديد هذا الخيار،[`PageSet`](../../fixedpagesaveoptions/pageset/) يتم تجاهله عند الحفظ. يتطابق هذا السلوك مع MS Word. إذا لم يتم تحديد إعدادات طباعة طي الكتاب في إعداد الصفحة، فلن يكون لهذا الخيار أي تأثير.

## أمثلة

يوضح كيفية حفظ مستند بتنسيق PDF في شكل كتاب مطوي.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "UseBookFoldPrintingSettings" على "true" لترتيب المحتويات
// في ملف PDF الناتج بطريقة تساعدنا على استخدامه لإنشاء كتيب.
// قم بضبط خاصية "UseBookFoldPrintingSettings" على "false" لعرض ملف PDF بشكل طبيعي.
options.UseBookFoldPrintingSettings = renderTextAsBookfold;

// إذا كنا نعرض المستند ككتيب، فيجب علينا تعيين "صفحات متعددة"
// خصائص كائنات إعداد الصفحة لجميع الأقسام إلى "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookfold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// بمجرد طباعة هذا المستند على جانبي الصفحات، يمكننا طي جميع الصفحات من المنتصف مرة واحدة،
//وسوف يتم ترتيب المحتويات بطريقة تؤدي إلى إنشاء كتيب.
doc.Save(ArtifactsDir + "PdfSaveOptions.SaveAsPdfBookFold.pdf", options);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
