---
title: ImageSaveOptions.ImageSize
second_title: Aspose.Words لمراجع .NET API
description: ImageSaveOptions ملكية. الحصول على أو تعيين حجم الصورة التي تم إنشاؤها بالبكسل.
type: docs
weight: 70
url: /ar/net/aspose.words.saving/imagesaveoptions/imagesize/
---
## ImageSaveOptions.ImageSize property

الحصول على أو تعيين حجم الصورة التي تم إنشاؤها بالبكسل.

```csharp
public Size ImageSize { get; set; }
```

### ملاحظات

تؤثر هذه الخاصية فقط عند الحفظ في تنسيقات الصور النقطية.

القيمة الافتراضية هي (0 × 0)، مما يعني أنه سيتم حساب حجم الصورة المولدة وفقًا لحجم الصورة بالنقاط، والدقة والمقياس المحددين.

### أمثلة

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

// أنشئ كائن "ImageSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل الطريقة التي تعرض بها هذه الطريقة المستند إلى صورة.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // قم بتعيين خاصية "PageSet" على رقم الصفحة الأولى من
    // الذي يبدأ عرض المستند منه.
    options.PageSet = new PageSet(i);
    // تصدير الصفحة بحجم 2325 × 5325 بكسل و600 نقطة في البوصة.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

### أنظر أيضا

* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../imagesaveoptions/)
* المجسم [Aspose.Words](../../../)


