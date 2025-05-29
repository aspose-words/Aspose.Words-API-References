---
title: ImageSaveOptions.PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ImageSaveOptions PageSet لتخصيص عرض مستندك. حدّد الصفحات التي تريد حفظها للحصول على مخرجات مُحسّنة. استكشف الآن!
type: docs
weight: 100
url: /ar/net/aspose.words.saving/imagesaveoptions/pageset/
---
## ImageSaveOptions.PageSet property

يحصل على الصفحات التي سيتم عرضها أو يعينها. الافتراضي هو كل الصفحات الموجودة في المستند.

```csharp
public PageSet PageSet { get; set; }
```

## ملاحظات

هذه الخاصية سارية فقط عند عرض صفحات المستندات. يتم تجاهلها عند عرض الأشكال على الصور.

## أمثلة

يوضح كيفية استخراج الصفحات استنادًا إلى نطاقات الصفحات الدقيقة.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

يوضح كيفية تحديد الصفحة في المستند التي سيتم عرضها كصورة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world! This is page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("This is page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("This is page 3.");

Assert.AreEqual(3, doc.PageCount);

// عندما نحفظ المستند كصورة، يقوم Aspose.Words بعرض الصفحة الأولى فقط بشكل افتراضي.
// يمكننا تمرير كائن SaveOptions لتحديد صفحة مختلفة لعرضها.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Gif);
// تحويل كل صفحة من المستند إلى ملف صورة منفصل.
for (int i = 1; i <= doc.PageCount; i++)
{
    saveOptions.PageSet = new PageSet(1);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageIndex.Page {i}.gif", saveOptions);
}
```

يوضح كيفية عرض كل صفحة من المستند إلى صورة TIFF منفصلة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// قم بإنشاء كائن "ImageSaveOptions" الذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل الطريقة التي تقوم بها هذه الطريقة بتحويل المستند إلى صورة.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // اضبط خاصية "PageSet" على رقم الصفحة الأولى من
    // الذي سيتم البدء في عرض المستند منه.
    options.PageSet = new PageSet(i);
    // تصدير الصفحة بدقة 2325 × 5325 بكسل و 600 نقطة في البوصة.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

يوضح كيفية عرض صفحة واحدة من مستند إلى صورة JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// قم بإنشاء كائن "ImageSaveOptions" الذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل الطريقة التي تقوم بها هذه الطريقة بتحويل المستند إلى صورة.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// اضبط "PageSet" على "1" لتحديد الصفحة الثانية عبر
// الفهرس المبني على الصفر لبدء عرض المستند منه.
options.PageSet = new PageSet(1);

// عندما نحفظ المستند بتنسيق JPEG، يقوم Aspose.Words بعرض صفحة واحدة فقط.
// ستحتوي هذه الصورة على صفحة واحدة بدءًا من الصفحة الثانية،
// والتي ستكون فقط الصفحة الثانية من المستند الأصلي.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### أنظر أيضا

* class [PageSet](../../pageset/)
* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
