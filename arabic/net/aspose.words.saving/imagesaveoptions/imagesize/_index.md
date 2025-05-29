---
title: ImageSaveOptions.ImageSize
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ImageSize في ImageSaveOptions لإدارة أبعاد الصورة وتخصيصها بالبكسل بسهولة للحصول على أفضل النتائج.
type: docs
weight: 70
url: /ar/net/aspose.words.saving/imagesaveoptions/imagesize/
---
## ImageSaveOptions.ImageSize property

يحصل على حجم الصورة المولدة بالبكسل أو يعينه.

```csharp
public Size ImageSize { get; set; }
```

## ملاحظات

لا يكون لهذه الخاصية تأثير إلا عند الحفظ بتنسيقات الصور النقطية.

القيمة الافتراضية هي (0 × 0)، مما يعني أن حجم الصورة المولدة سيتم حسابه وفقًا لحجم الصورة بالنقاط والدقة والمقياس المحددين.

## أمثلة

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

### أنظر أيضا

* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
