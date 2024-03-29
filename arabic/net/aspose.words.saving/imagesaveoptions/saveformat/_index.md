---
title: ImageSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words لـ .NET
description: ImageSaveOptions SaveFormat ملكية. يحدد التنسيق الذي سيتم به حفظ صفحات أو أشكال المستند المقدمة إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن يكون raster Tiff Png BmpJpeg أو ناقلاتEmf EpsSvg  في C#.
type: docs
weight: 140
url: /ar/net/aspose.words.saving/imagesaveoptions/saveformat/
---
## ImageSaveOptions.SaveFormat property

يحدد التنسيق الذي سيتم به حفظ صفحات أو أشكال المستند المقدمة إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن يكون raster Tiff ,Png ,BmpJpeg أو ناقلاتEmf ,EpsSvg .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## ملاحظات

يعتمد عدد الخيارات الأخرى على التنسيق المحدد.

ومن الممكن أيضًا الحفظ إلى SVG عبر كليهما[`ImageSaveOptions`](../) وعبر[`SvgSaveOptions`](../../svgsaveoptions/).

## أمثلة

يوضح كيفية تحرير الصورة بينما يقوم Aspose.Words بتحويل مستند إلى مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// عندما نحفظ المستند كصورة، يمكننا تمرير كائن SaveOptions إليه
// قم بتحرير الصورة أثناء عرضها من خلال عملية الحفظ.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // يمكننا ضبط هذه الخصائص لتغيير سطوع الصورة وتباينها.
    // كلاهما على مقياس من 0 إلى 1 ويكونا عند 0.5 بشكل افتراضي.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // يمكننا ضبط الدقة الأفقية والرأسية باستخدام هذه الخصائص.
    // سيؤثر هذا على أبعاد الصورة.
    // القيمة الافتراضية لهذه الخصائص هي 96.0، بدقة 96 نقطة في البوصة.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // يمكننا تغيير حجم الصورة باستخدام هذه الخاصية. القيمة الافتراضية هي 1.0، للقياس بنسبة 100%.
    // يمكننا استخدام هذه الخاصية لإلغاء أي تغييرات في أبعاد الصورة قد يسببها تغيير الدقة.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
