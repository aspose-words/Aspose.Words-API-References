---
title: PsSaveOptions.SaveFormat
second_title: Aspose.Words لمراجع .NET API
description: PsSaveOptions ملكية. يحدد التنسيق الذي سيتم حفظ المستند به في حالة استخدام كائن خيارات الحفظ هذا. يمكن أن يكون فقطPs .
type: docs
weight: 20
url: /ar/net/aspose.words.saving/pssaveoptions/saveformat/
---
## PsSaveOptions.SaveFormat property

يحدد التنسيق الذي سيتم حفظ المستند به في حالة استخدام كائن خيارات الحفظ هذا. يمكن أن يكون فقطPs .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PsSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../pssaveoptions/)
* المجسم [Aspose.Words](../../../)


