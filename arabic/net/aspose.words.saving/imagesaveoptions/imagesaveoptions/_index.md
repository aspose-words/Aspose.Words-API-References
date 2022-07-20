---
title: ImageSaveOptions
second_title: Aspose.Words لمراجع .NET API
description: تهيئة مثيل جديد من هذه الفئة يمكن استخدامه لحفظ الصور المعروضة في Tiff وPng وBmp  Emf وJpeg أوSvg التنسيق ._ x000d_Png وBmp وJpeg أوSvg التنسيق ._ x000d_
type: docs
weight: 10
url: /ar/net/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions constructor

تهيئة مثيل جديد من هذه الفئة يمكن استخدامه لحفظ الصور المعروضة في Tiff وPng وBmp ، Emf وJpeg أوSvg التنسيق ._ x000d_Png وBmp وJpeg أوSvg التنسيق ._ x000d_

```csharp
public ImageSaveOptions(SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| saveFormat | SaveFormat | يمكن أن يكون Tiff وPng وBmp ، Emf وJpeg أوSvg . Png وBmp وJpeg أوSvg . |

### أمثلة

يوضح كيفية تكوين الضغط أثناء حفظ مستند بتنسيق JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// قم بإنشاء كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل الطريقة التي تعرض بها هذه الطريقة المستند إلى صورة.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// اضبط خاصية "JpegQuality" على "10" لاستخدام ضغط أقوى عند تقديم المستند.
// سيؤدي ذلك إلى تقليل حجم ملف المستند ، لكن الصورة ستعرض المزيد من عناصر الضغط البارزة.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// اضبط خاصية "JpegQuality" على "100" لاستخدام ضغط أضعف عند تمزيق المستند.
// سيؤدي ذلك إلى تحسين جودة الصورة على حساب زيادة حجم الملف.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat)
* class [ImageSaveOptions](../../imagesaveoptions)
* مساحة الاسم [Aspose.Words.Saving](../../imagesaveoptions)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->