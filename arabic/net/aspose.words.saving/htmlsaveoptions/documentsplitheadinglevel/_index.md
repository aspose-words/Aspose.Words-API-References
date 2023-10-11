---
title: HtmlSaveOptions.DocumentSplitHeadingLevel
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يحدد الحد الأقصى لمستوى العناوين التي سيتم عندها تقسيم المستند. القيمة الافتراضية هي2 .
type: docs
weight: 90
url: /ar/net/aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/
---
## HtmlSaveOptions.DocumentSplitHeadingLevel property

يحدد الحد الأقصى لمستوى العناوين التي سيتم عندها تقسيم المستند. القيمة الافتراضية هي`2` .

```csharp
public int DocumentSplitHeadingLevel { get; set; }
```

### ملاحظات

متى[`DocumentSplitCriteria`](../documentsplitcriteria/) يشملHeadingParagraph وتم ضبط هذه الخاصية على قيمة من 1 إلى 9، سيتم تقسيم المستند إلى فقرات منسقة باستخدام  **عنوان 1** , **العنوان 2** , **العنوان 3**إلخ. الأنماط تصل إلى مستوى العنوان المحدد.

افتراضيا فقط **عنوان 1** و **العنوان 2** تؤدي الفقرات إلى تقسيم المستند. سيؤدي تعيين هذه الخاصية إلى الصفر إلى عدم تقسيم المستند عند فقرات العناوين على الإطلاق.

### أمثلة

يوضح كيفية تقسيم مستند HTML الناتج عن طريق العناوين إلى عدة أجزاء.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// كل فقرة نقوم بتنسيقها باستخدام نمط "العنوان" يمكن أن تكون بمثابة عنوان.
// قد يكون لكل عنوان أيضًا مستوى عنوان، يتم تحديده من خلال عدد نمط العنوان الخاص به.
// العناوين أدناه هي من المستويات 1-3.
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #1");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #2");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #3");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #4");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #5");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #6");

// قم بإنشاء كائن HtmlSaveOptions وقم بتعيين معايير التقسيم على "HeadingParagraph".
// ستؤدي هذه المعايير إلى تقسيم المستند في الفقرات ذات أنماط "العناوين" إلى عدة مستندات أصغر،
// واحفظ كل مستند في ملف HTML منفصل في نظام الملفات المحلي.
// سنقوم أيضًا بتعيين الحد الأقصى لمستوى العنوان، والذي يقسم المستند إلى 2.
// سيؤدي حفظ المستند إلى تقسيمه عند عناوين المستويات 1 و2، ولكن ليس عند العناوين من 3 إلى 9.
HtmlSaveOptions options = new HtmlSaveOptions
{
    DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph,
    DocumentSplitHeadingLevel = 2
};

// تحتوي وثيقتنا على أربعة عناوين للمستويات 1 - 2. ولن يكون أحد هذه العناوين
// نقطة الانقسام لأنها في بداية المستند.
// ستؤدي عملية الحفظ إلى تقسيم المستند الخاص بنا في ثلاثة أماكن إلى أربع مستندات أصغر.
doc.Save(ArtifactsDir + "HtmlSaveOptions.HeadingLevels.html", options);

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels.html");

Assert.AreEqual("Heading #1", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-01.html");

Assert.AreEqual("Heading #2\r" +
                "Heading #3", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-02.html");

Assert.AreEqual("Heading #4", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-03.html");

Assert.AreEqual("Heading #5\r" +
                "Heading #6", doc.GetText().Trim());
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


