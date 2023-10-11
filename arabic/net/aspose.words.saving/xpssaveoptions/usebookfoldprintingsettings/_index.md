---
title: XpsSaveOptions.UseBookFoldPrintingSettings
second_title: Aspose.Words لمراجع .NET API
description: XpsSaveOptions ملكية. الحصول على قيمة منطقية أو تعيينها تشير إلى ما إذا كان يجب حفظ المستند باستخدام تخطيط طباعة الكتيبات إذا تم تحديده عبرMultiplePages .
type: docs
weight: 40
url: /ar/net/aspose.words.saving/xpssaveoptions/usebookfoldprintingsettings/
---
## XpsSaveOptions.UseBookFoldPrintingSettings property

الحصول على قيمة منطقية أو تعيينها تشير إلى ما إذا كان يجب حفظ المستند باستخدام تخطيط طباعة الكتيبات، إذا تم تحديده عبر[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

### ملاحظات

إذا تم تحديد هذا الخيار،[`PageSet`](../../fixedpagesaveoptions/pageset/) يتم تجاهله عند الحفظ. يتطابق هذا السلوك مع MS Word. إذا لم يتم تحديد إعدادات طباعة طي الكتاب في إعداد الصفحة، فلن يكون لهذا الخيار أي تأثير.

### أمثلة

يوضح كيفية حفظ مستند بتنسيق XPS على شكل طية كتاب.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// قم بإنشاء كائن "XpsSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذا الأسلوب للمستند إلى .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// اضبط خاصية "UseBookFoldPrintingSettings" على "صحيح" لترتيب المحتويات
// في مخرجات XPS بطريقة تساعدنا على استخدامها لعمل كتيب.
// قم بتعيين خاصية "UseBookFoldPrintingSettings" على "خطأ" لعرض XPS بشكل طبيعي.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// إذا كنا نعرض المستند ككتيب، فيجب علينا تعيين "الصفحات المتعددة"
// خصائص كائنات إعداد الصفحة لجميع الأقسام إلى "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// بمجرد طباعة هذه الوثيقة، يمكننا تحويلها إلى كتيب عن طريق تكديس الصفحات
// للخروج من الطابعة والطي في المنتصف.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### أنظر أيضا

* class [XpsSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../xpssaveoptions/)
* المجسم [Aspose.Words](../../../)


