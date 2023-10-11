---
title: ImageSaveOptions.ImageSaveOptions
second_title: Aspose.Words لمراجع .NET API
description: ImageSaveOptions البناء. تهيئة مثيل جديد لهذه الفئة والذي يمكن استخدامه لحفظ الصور المعروضة في Tiff Png BmpJpeg Emf Eps أوSvg التنسيق.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions constructor

تهيئة مثيل جديد لهذه الفئة والذي يمكن استخدامه لحفظ الصور المعروضة في Tiff ,Png ,BmpJpeg ,Emf ,Eps أوSvg التنسيق.

```csharp
public ImageSaveOptions(SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| saveFormat | SaveFormat | يمكن أن يكون Tiff ,Png ,BmpJpeg ,Emf ,Eps أوSvg التنسيق. |

### أمثلة

يوضح كيفية تكوين الضغط أثناء حفظ مستند بتنسيق JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// أنشئ كائن "ImageSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل الطريقة التي تعرض بها هذه الطريقة المستند إلى صورة.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// اضبط خاصية "JpegQuality" على "10" لاستخدام ضغط أقوى عند عرض المستند.
// سيؤدي هذا إلى تقليل حجم ملف المستند، لكن الصورة ستعرض عناصر ضغط أكثر وضوحًا.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// اضبط خاصية "JpegQuality" على "100" لاستخدام ضغط أضعف عند تقطيع المستند.
// سيؤدي هذا إلى تحسين جودة الصورة على حساب زيادة حجم الملف.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../imagesaveoptions/)
* المجسم [Aspose.Words](../../../)


