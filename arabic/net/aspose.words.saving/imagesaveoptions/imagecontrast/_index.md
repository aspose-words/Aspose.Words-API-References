---
title: ImageSaveOptions.ImageContrast
linktitle: ImageContrast
articleTitle: ImageContrast
second_title: Aspose.Words لـ .NET
description: اضبط خاصية ImageContrast في ImageSaveOptions لتحسين وضوح صورك وعمقها. حسّن صورك بكل سهولة!
type: docs
weight: 60
url: /ar/net/aspose.words.saving/imagesaveoptions/imagecontrast/
---
## ImageSaveOptions.ImageContrast property

يحصل على التباين للصور المولدة أو يضبطه.

```csharp
public float ImageContrast { get; set; }
```

## ملاحظات

لا يكون لهذه الخاصية تأثير إلا عند الحفظ بتنسيقات الصور النقطية.

القيمة الافتراضية هي ٠٫٥. يجب أن تكون القيمة بين ٠ و١.

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

* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
