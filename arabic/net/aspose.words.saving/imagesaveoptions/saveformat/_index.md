---
title: ImageSaveOptions.SaveFormat
second_title: Aspose.Words لمراجع .NET API
description: ImageSaveOptions ملكية. يحدد التنسيق الذي سيتم به حفظ صفحات المستند أو الأشكال المعروضة إذا تم استخدام كائن خيارات الحفظ هذا.Tiff وPng وBmp  Jpeg أو ناقلEmf وSvg .
type: docs
weight: 130
url: /ar/net/aspose.words.saving/imagesaveoptions/saveformat/
---
## ImageSaveOptions.SaveFormat property

يحدد التنسيق الذي سيتم به حفظ صفحات المستند أو الأشكال المعروضة إذا تم استخدام كائن خيارات الحفظ هذا.Tiff وPng وBmp ، Jpeg أو ناقلEmf وSvg .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### ملاحظات

في الأنظمة الأساسية المختلفة ، قد تكون التنسيقات المدعومة مختلفة. يعتمد عدد الخيارات الأخرى على التنسيق المحدد.

أيضًا ، من الممكن الحفظ في SVG عبر ImageSaveOptions وعبر[`SvgSaveOptions`](../../svgsaveoptions/).

### أمثلة

يوضح كيفية تحرير الصورة بينما يقوم Aspose.Words بتحويل مستند إلى واحد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// عندما نحفظ المستند كصورة ، يمكننا تمرير كائن SaveOptions إليه
// تحرير الصورة بينما تعرضها عملية الحفظ.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // يمكننا ضبط هذه الخصائص لتغيير سطوع الصورة وتباينها.
    // كلاهما على مقياس 0-1 وهما 0.5 افتراضيًا.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // يمكننا ضبط الدقة الأفقية والعمودية بهذه الخصائص.
    // سيؤثر هذا على أبعاد الصورة.
    // القيمة الافتراضية لهذه الخصائص هي 96.0 ، لدقة 96 نقطة في البوصة.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // يمكننا قياس الصورة باستخدام هذه الخاصية. القيمة الافتراضية هي 1.0 للقياس بنسبة 100٪.
    // يمكننا استخدام هذه الخاصية لإلغاء أي تغييرات في أبعاد الصورة قد يسببها تغيير الدقة.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../imagesaveoptions/)
* المجسم [Aspose.Words](../../../)


