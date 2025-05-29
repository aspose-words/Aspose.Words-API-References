---
title: ImageSaveOptions.Scale
linktitle: Scale
articleTitle: Scale
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ImageSaveOptions Scale لضبط عامل التكبير/التصغير لصورك بسهولة، مما يعزز الجودة والتخصيص.
type: docs
weight: 150
url: /ar/net/aspose.words.saving/imagesaveoptions/scale/
---
## ImageSaveOptions.Scale property

يحصل على عامل التكبير/التصغير للصور المُولدة أو يضبطه.

```csharp
public float Scale { get; set; }
```

## ملاحظات

القيمة الافتراضية هي ١.٠. يجب أن تكون القيمة أكبر من ٠.

## أمثلة

يوضح كيفية تحويل كائن Office Math إلى ملف صورة في نظام الملفات المحلي.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// قم بإنشاء كائن "ImageSaveOptions" لتمريره إلى طريقة "Save" الخاصة بمقدم العقدة لتعديلها
// كيف يتم تحويل عقدة OfficeMath إلى صورة.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// اضبط خاصية "المقياس" على 5 لجعل الكائن أكبر بخمس مرات من حجمه الأصلي.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

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
