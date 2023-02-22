---
title: ImageSaveOptions.PageSet
second_title: Aspose.Words لمراجع .NET API
description: ImageSaveOptions ملكية. الحصول على الصفحات المراد عرضها أو تعيينها. الإعداد الافتراضي هو كافة الصفحات الموجودة في المستند.
type: docs
weight: 90
url: /ar/net/aspose.words.saving/imagesaveoptions/pageset/
---
## ImageSaveOptions.PageSet property

الحصول على الصفحات المراد عرضها أو تعيينها. الإعداد الافتراضي هو كافة الصفحات الموجودة في المستند.

```csharp
public PageSet PageSet { get; set; }
```

### ملاحظات

هذه الخاصية لها تأثير فقط عند تقديم صفحات الوثيقة. يتم تجاهل هذه الخاصية عند عرض الأشكال على الصور.

### أمثلة

يوضح كيفية استخراج الصفحات بناءً على نطاقات الصفحات الدقيقة.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

يوضح كيفية تجسيد كل صفحة من المستند إلى صورة TIFF منفصلة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// قم بإنشاء كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل الطريقة التي تعرض بها هذه الطريقة المستند إلى صورة.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // قم بتعيين خاصية "PageSet" على رقم الصفحة الأولى من
    // الذي يبدأ عرض المستند منه.
    options.PageSet = new PageSet(i);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

يوضح كيفية تحديد أي صفحة في مستند يتم عرضها كصورة.

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

// عندما نحفظ المستند كصورة ، يعرض Aspose.Words الصفحة الأولى بشكل افتراضي فقط.
// يمكننا تمرير كائن SaveOptions لتحديد صفحة مختلفة لعرضها.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Gif);

// تقديم كل صفحة من المستند إلى ملف صورة منفصل.
for (int i = 1; i <= doc.PageCount; i++)
{
    saveOptions.PageSet = new PageSet(1);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageIndex.Page {i}.gif", saveOptions);
}
```

يوضح كيفية تجسيد صفحة واحدة من مستند إلى صورة بتنسيق JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// قم بإنشاء كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل الطريقة التي تعرض بها هذه الطريقة المستند إلى صورة.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);

// اضبط "PageSet" على "1" لتحديد الصفحة الثانية عبر
// الفهرس الصفري لبدء عرض المستند منه.
options.PageSet = new PageSet(1);

// عندما نحفظ المستند بتنسيق JPEG ، يعرض Aspose.Words صفحة واحدة فقط.
// ستحتوي هذه الصورة على صفحة واحدة تبدأ من الصفحة الثانية ،
// والتي ستكون فقط الصفحة الثانية من المستند الأصلي.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### أنظر أيضا

* class [PageSet](../../pageset/)
* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../imagesaveoptions/)
* المجسم [Aspose.Words](../../../)


