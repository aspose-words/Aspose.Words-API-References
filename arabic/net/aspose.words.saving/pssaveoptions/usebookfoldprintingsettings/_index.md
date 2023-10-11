---
title: PsSaveOptions.UseBookFoldPrintingSettings
second_title: Aspose.Words لمراجع .NET API
description: PsSaveOptions ملكية. الحصول على قيمة منطقية أو تعيينها تشير إلى ما إذا كان يجب حفظ المستند باستخدام تخطيط طباعة الكتيبات إذا تم تحديده عبرMultiplePages .
type: docs
weight: 30
url: /ar/net/aspose.words.saving/pssaveoptions/usebookfoldprintingsettings/
---
## PsSaveOptions.UseBookFoldPrintingSettings property

الحصول على قيمة منطقية أو تعيينها تشير إلى ما إذا كان يجب حفظ المستند باستخدام تخطيط طباعة الكتيبات، إذا تم تحديده عبر[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

### ملاحظات

إذا تم تحديد هذا الخيار،[`PageSet`](../../fixedpagesaveoptions/pageset/) يتم تجاهله عند الحفظ. يتطابق هذا السلوك مع MS Word. إذا لم يتم تحديد إعدادات طباعة طي الكتاب في إعداد الصفحة، فلن يكون لهذا الخيار أي تأثير.

### أمثلة

يوضح كيفية حفظ مستند بتنسيق Postscript على شكل طية كتاب.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// أنشئ كائن "PsSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى PostScript.
// اضبط خاصية "UseBookFoldPrintingSettings" على "صحيح" لترتيب المحتويات
// في مستند Postscript الناتج بطريقة تساعدنا في إنشاء كتيب منه.
// اضبط خاصية "UseBookFoldPrintingSettings" على "خطأ" لحفظ المستند بشكل طبيعي.
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// إذا كنا نعرض المستند ككتيب، فيجب علينا تعيين "الصفحات المتعددة"
// خصائص كائنات إعداد الصفحة لجميع الأقسام إلى "MultiplePagesType.BookFoldPrinting".
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// بمجرد طباعة هذه الوثيقة على جانبي الصفحات، يمكننا طي جميع الصفحات إلى المنتصف مرة واحدة،
// وسوف تصطف المحتويات بطريقة تُنشئ كتيبًا.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### أنظر أيضا

* class [PsSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../pssaveoptions/)
* المجسم [Aspose.Words](../../../)


