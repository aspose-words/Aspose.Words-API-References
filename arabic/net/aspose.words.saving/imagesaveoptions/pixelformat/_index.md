---
title: ImageSaveOptions.PixelFormat
linktitle: PixelFormat
articleTitle: PixelFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PixelFormat في ImageSaveOptions لتخصيص تنسيق البكسل للصور التي تم إنشاؤها بسهولة للحصول على الجودة والأداء الأمثل.
type: docs
weight: 120
url: /ar/net/aspose.words.saving/imagesaveoptions/pixelformat/
---
## ImageSaveOptions.PixelFormat property

يحصل على تنسيق البكسل للصور المولدة أو يعينه.

```csharp
public ImagePixelFormat PixelFormat { get; set; }
```

## ملاحظات

لا يكون لهذه الخاصية تأثير إلا عند الحفظ بتنسيقات الصور النقطية.

القيمة الافتراضية هيFormat32BppArgb.

قد يختلف تنسيق البكسل للصورة الناتجة عن القيمة المحددة بسبب عمل GDI+.

## أمثلة

يوضح كيفية تحديد معدل البت لكل بكسل الذي سيتم به تحويل المستند إلى صورة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// عندما نحفظ المستند كصورة، يمكننا تمرير كائن SaveOptions إلى
// حدد تنسيق البكسل للصورة التي سيتم إنشاءها من خلال عملية الحفظ.
// ستؤثر معدلات البت المختلفة لكل بكسل على جودة وحجم ملف الصورة المولدة.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

//يمكننا استنساخ مثيلات ImageSaveOptions.
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### أنظر أيضا

* enum [ImagePixelFormat](../../imagepixelformat/)
* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
