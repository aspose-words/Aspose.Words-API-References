---
title: ImageSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية SaveFormat في ImageSaveOptions لحفظ المستندات بسهولة بتنسيقات مثل TIFF وPNG وJPEG وغيرها. حسّن سير عملك اليوم!
type: docs
weight: 140
url: /ar/net/aspose.words.saving/imagesaveoptions/saveformat/
---
## ImageSaveOptions.SaveFormat property

يحدد التنسيق الذي سيتم به حفظ صفحات المستند أو الأشكال المقدمة إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن يكون raster Tiff ،Png ،Bmp ، Jpeg أو متجهEmf ،Eps ، WebP ،Svg .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## ملاحظات

يعتمد عدد الخيارات الأخرى على التنسيق المحدد.

كما أنه من الممكن الحفظ إلى SVG عبر[`ImageSaveOptions`](../) وعبر[`SvgSaveOptions`](../../svgsaveoptions/).

## أمثلة

يوضح كيفية تحرير الصورة أثناء قيام Aspose.Words بتحويل مستند إلى صورة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// عندما نحفظ المستند كصورة، يمكننا تمرير كائن SaveOptions إلى
// قم بتحرير الصورة أثناء قيام عملية الحفظ بعرضها.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    //يمكننا تعديل هذه الخصائص لتغيير سطوع الصورة وتباينها.
    // كلاهما على مقياس من 0 إلى 1 ويكونان عند 0.5 بشكل افتراضي.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    //يمكننا ضبط الدقة الأفقية والرأسية باستخدام هذه الخصائص.
    //سيؤثر هذا على أبعاد الصورة.
    // القيمة الافتراضية لهذه الخصائص هي 96.0، لدقة 96 نقطة في البوصة.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // يمكننا تغيير حجم الصورة باستخدام هذه الخاصية. القيمة الافتراضية هي 1.0، لضبط الحجم بنسبة 100%.
    // يمكننا استخدام هذه الخاصية لإلغاء أي تغييرات في أبعاد الصورة التي قد يسببها تغيير الدقة.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
