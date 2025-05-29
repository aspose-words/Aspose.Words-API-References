---
title: XpsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words لـ .NET
description: قم بتحسين تخطيط مستندك باستخدام خاصية XpsSaveOptions UseBookFoldPrintingSettings، مما يتيح لك طباعة كتيبات سلسة لتقديم عرض محسّن.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/xpssaveoptions/usebookfoldprintingsettings/
---
## XpsSaveOptions.UseBookFoldPrintingSettings property

يحصل على قيمة منطقية أو يعينها للإشارة إلى ما إذا كان يجب حفظ المستند باستخدام تخطيط طباعة الكتيبات، إذا تم تحديد ذلك عبر[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## ملاحظات

إذا تم تحديد هذا الخيار،[`PageSet`](../../fixedpagesaveoptions/pageset/) يتم تجاهله عند الحفظ. يتطابق هذا السلوك مع MS Word. إذا لم يتم تحديد إعدادات طباعة طي الكتاب في إعداد الصفحة، فلن يكون لهذا الخيار أي تأثير.

## أمثلة

يوضح كيفية حفظ مستند بتنسيق XPS في شكل كتاب مطوي.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// قم بإنشاء كائن "XpsSaveOptions" الذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// اضبط خاصية "UseBookFoldPrintingSettings" على "true" لترتيب المحتويات
// في إخراج XPS بطريقة تساعدنا على استخدامه لإنشاء كتيب.
// قم بضبط خاصية "UseBookFoldPrintingSettings" على "false" لعرض XPS بشكل طبيعي.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// إذا كنا نعرض المستند ككتيب، فيجب علينا تعيين "صفحات متعددة"
// خصائص كائنات إعداد الصفحة لجميع الأقسام إلى "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// بمجرد طباعة هذه الوثيقة، يمكننا تحويلها إلى كتيب عن طريق تكديس الصفحات
// للخروج من الطابعة وطيها من المنتصف.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### أنظر أيضا

* class [XpsSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
