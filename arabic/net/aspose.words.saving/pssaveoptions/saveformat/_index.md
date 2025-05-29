---
title: PsSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية SaveFormat في PsSaveOptions لتحديد تنسيق حفظ مستندك بسهولة. حسّن سير عملك مع خيارات حفظ مرنة!
type: docs
weight: 20
url: /ar/net/aspose.words.saving/pssaveoptions/saveformat/
---
## PsSaveOptions.SaveFormat property

يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا. لا يمكن أن يكون إلاPs .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PsSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
