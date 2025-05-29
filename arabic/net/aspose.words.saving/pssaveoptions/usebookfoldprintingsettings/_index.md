---
title: PsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PsSaveOptions UseBookFoldPrintingSettings لحفظ المستندات بسهولة في تخطيط كتيب لتحسين كفاءة الطباعة.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/pssaveoptions/usebookfoldprintingsettings/
---
## PsSaveOptions.UseBookFoldPrintingSettings property

يحصل على قيمة منطقية أو يعينها للإشارة إلى ما إذا كان يجب حفظ المستند باستخدام تخطيط طباعة الكتيبات، إذا تم تحديد ذلك عبر[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## ملاحظات

إذا تم تحديد هذا الخيار،[`PageSet`](../../fixedpagesaveoptions/pageset/) يتم تجاهله عند الحفظ. يتطابق هذا السلوك مع MS Word. إذا لم يتم تحديد إعدادات طباعة طي الكتاب في إعداد الصفحة، فلن يكون لهذا الخيار أي تأثير.

## أمثلة

يوضح كيفية حفظ مستند بتنسيق Postscript في شكل طي الكتاب.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// قم بإنشاء كائن "PsSaveOptions" الذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى PostScript.
// اضبط خاصية "UseBookFoldPrintingSettings" على "true" لترتيب المحتويات
// في مستند Postscript الناتج بطريقة تساعدنا في إنشاء كتيب منه.
// قم بضبط الخاصية "UseBookFoldPrintingSettings" على "false" لحفظ المستند بشكل طبيعي.
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// إذا كنا نعرض المستند ككتيب، فيجب علينا تعيين "صفحات متعددة"
// خصائص كائنات إعداد الصفحة لجميع الأقسام إلى "MultiplePagesType.BookFoldPrinting".
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// بمجرد طباعة هذا المستند على جانبي الصفحات، يمكننا طي جميع الصفحات من المنتصف مرة واحدة،
//وسوف يتم ترتيب المحتويات بطريقة تؤدي إلى إنشاء كتيب.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### أنظر أيضا

* class [PsSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
