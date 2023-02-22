---
title: HtmlSaveOptions.DocumentSplitHeadingLevel
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يحدد المستوى الأقصى للعناوين التي يتم عندها تقسيم المستند. القيمة الافتراضية هي2 .
type: docs
weight: 90
url: /ar/net/aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/
---
## HtmlSaveOptions.DocumentSplitHeadingLevel property

يحدد المستوى الأقصى للعناوين التي يتم عندها تقسيم المستند. القيمة الافتراضية هي`2` .

```csharp
public int DocumentSplitHeadingLevel { get; set; }
```

### ملاحظات

متي[`DocumentSplitCriteria`](../documentsplitcriteria/) يشملHeadingParagraph وهذه الخاصية مضبوطة على قيمة من 1 إلى 9 ، سيتم تقسيم المستند على فقرات منسقة باستخدام  **عنوان 1** و **العنوان 2** و **العنوان 3** إلخ تصل إلى مستوى العنوان المحدد.

بشكل افتراضي ، فقط **عنوان 1** و **العنوان 2** الفقرات تؤدي إلى تقسيم المستند. سيؤدي تعيين هذه الخاصية إلى الصفر إلى عدم تقسيم المستند عند فقرات العنوان على الإطلاق.

### أمثلة

يوضح كيفية تقسيم مستند HTML الناتج عن طريق العناوين إلى عدة أجزاء.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// كل فقرة نقوم بتنسيقها باستخدام نمط "العنوان" يمكن أن تكون بمثابة عنوان.
// قد يكون لكل عنوان أيضًا مستوى عنوان محدد بواسطة رقم نمط العنوان الخاص به.
// العناوين أدناه من المستويات 1-3.
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

// قم بإنشاء كائن HtmlSaveOptions وقم بتعيين معايير الانقسام إلى "HeadingParagraph".
// ستقسم هذه المعايير المستند في فقرات بأنماط "العنوان" إلى عدة مستندات أصغر ،
// وحفظ كل مستند في ملف HTML منفصل في نظام الملفات المحلي.
// سنقوم أيضًا بتعيين الحد الأقصى لمستوى العنوان ، والذي يقسم المستند إلى 2.
// سيؤدي حفظ المستند إلى تقسيمه إلى عناوين المستويات 1 و 2 ، ولكن ليس في 3 إلى 9.
HtmlSaveOptions options = new HtmlSaveOptions
{
    DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph,
    DocumentSplitHeadingLevel = 2
};

// تحتوي وثيقتنا على أربعة عناوين من المستويات 1 - 2. لن يكون أحد هذه العناوين
// نقطة انقسام لأنها في بداية المستند.
// ستقسم عملية الحفظ وثيقتنا في ثلاثة أماكن ، إلى أربعة مستندات أصغر.
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


