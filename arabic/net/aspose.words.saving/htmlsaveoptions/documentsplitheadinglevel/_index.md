---
title: HtmlSaveOptions.DocumentSplitHeadingLevel
linktitle: DocumentSplitHeadingLevel
articleTitle: DocumentSplitHeadingLevel
second_title: Aspose.Words لـ .NET
description: حسّن تقسيم المستندات باستخدام DocumentSplitHeadingLevel في HtmlSaveOptions. تحكّم في مستويات العناوين لتحسين التنظيم. القيمة الافتراضية مضبوطة على ٢.
type: docs
weight: 90
url: /ar/net/aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/
---
## HtmlSaveOptions.DocumentSplitHeadingLevel property

يحدد الحد الأقصى لمستوى العناوين التي سيتم تقسيم المستند عندها. القيمة الافتراضية هي`2` .

```csharp
public int DocumentSplitHeadingLevel { get; set; }
```

## ملاحظات

متى[`DocumentSplitCriteria`](../documentsplitcriteria/) يشملHeadingParagraph وتم تعيين هذه الخاصية على قيمة من 1 إلى 9، سيتم تقسيم المستند عند الفقرات المنسقة باستخدام **العنوان 1** ،**العنوان 2** ،**العنوان 3**إلخ من الأنماط حتى مستوى العنوان المحدد.

افتراضيا، فقط**العنوان 1** و**العنوان 2** يؤدي تعيين هذه الخاصية إلى الصفر إلى عدم تقسيم المستند عند فقرات العنوان على الإطلاق.

## أمثلة

يوضح كيفية تقسيم مستند HTML الناتج حسب العناوين إلى عدة أجزاء.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// كل فقرة نقوم بتنسيقها باستخدام نمط "العنوان" يمكن أن تكون بمثابة عنوان.
// يمكن أن يكون لكل عنوان أيضًا مستوى عنوان، يتم تحديده من خلال رقم نمط العنوان الخاص به.
// العناوين أدناه هي للمستويات 1-3.
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

// قم بإنشاء كائن HtmlSaveOptions وقم بتعيين معايير التقسيم إلى "HeadingParagraph".
// ستعمل هذه المعايير على تقسيم المستند عند الفقرات ذات أنماط "العنوان" إلى عدة مستندات أصغر،
// وحفظ كل مستند في ملف HTML منفصل في نظام الملفات المحلي.
// سوف نقوم أيضًا بتعيين الحد الأقصى لمستوى العنوان، والذي يقوم بتقسيم المستند إلى 2.
// سيؤدي حفظ المستند إلى تقسيمه عند العناوين من المستويين 1 و2، ولكن ليس من 3 إلى 9.
HtmlSaveOptions options = new HtmlSaveOptions
{
    DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph,
    DocumentSplitHeadingLevel = 2
};

// تحتوي وثيقتنا على أربعة عناوين من المستويين 1 - 2. لن يتم تضمين أحد هذه العناوين
// نقطة تقسيم لأنها في بداية المستند.
// ستعمل عملية الحفظ على تقسيم مستندنا في ثلاثة أماكن، إلى أربعة مستندات أصغر.
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
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
