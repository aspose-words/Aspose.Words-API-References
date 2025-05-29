---
title: ImageSaveOptions
linktitle: ImageSaveOptions
articleTitle: ImageSaveOptions
second_title: Aspose.Words لـ .NET
description: اكتشف مُنشئ ImageSaveOptions لحفظ الصور بتنسيقات متعددة مثل TIFF وPNG وBMP وJPEG وEMF وEPS وWebP وSVG. حسّن تعاملك مع الصور!
type: docs
weight: 10
url: /ar/net/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions constructor

يقوم بتهيئة مثيل جديد لهذه الفئة التي يمكن استخدامها لحفظ الصور المقدمة في Tiff ،Png ،Bmp ، Jpeg ،Emf ،Eps ، WebP أوSvg تنسيق.

```csharp
public ImageSaveOptions(SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| saveFormat | SaveFormat | يمكن أن يكون Tiff ،Png ،Bmp ، Jpeg ،Emf ،EpsWebP أوSvg تنسيق. |

## أمثلة

يوضح كيفية تكوين الضغط أثناء حفظ مستند بتنسيق JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// قم بإنشاء كائن "ImageSaveOptions" الذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل الطريقة التي تقوم بها هذه الطريقة بتحويل المستند إلى صورة.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// قم بضبط خاصية "JpegQuality" على "10" لاستخدام ضغط أقوى عند عرض المستند.
// سيؤدي هذا إلى تقليل حجم ملف المستند، ولكن الصورة ستعرض آثار ضغط أكثر وضوحًا.
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// قم بضبط خاصية "JpegQuality" على "100" لاستخدام ضغط أضعف عند عرض المستند.
// سيؤدي هذا إلى تحسين جودة الصورة على حساب زيادة حجم الملف.
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
