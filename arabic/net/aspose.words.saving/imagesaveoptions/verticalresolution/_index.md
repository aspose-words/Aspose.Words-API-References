---
title: ImageSaveOptions.VerticalResolution
linktitle: VerticalResolution
articleTitle: VerticalResolution
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ImageSaveOptions VerticalResolution لضبط جودة الصورة بدقة DPI وتحسينها بسهولة، للحصول على صور مذهلة. حسّن مشاريعك اليوم!
type: docs
weight: 200
url: /ar/net/aspose.words.saving/imagesaveoptions/verticalresolution/
---
## ImageSaveOptions.VerticalResolution property

يحصل على الدقة الرأسية للصور المولدة أو يضبطها، بنقاط لكل بوصة.

```csharp
public float VerticalResolution { get; set; }
```

## ملاحظات

لا تؤثر هذه الخاصية إلا عند الحفظ بتنسيقات الصور النقطية وتؤثر على حجم الإخراج بالبكسل.

القيمة الافتراضية هي 96.

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
