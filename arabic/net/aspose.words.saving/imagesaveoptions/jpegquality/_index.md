---
title: ImageSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words لـ .NET
description: ImageSaveOptions JpegQuality ملكية. الحصول على أو تعيين قيمة تحدد جودة صور JPEG التي تم إنشاؤها في C#.
type: docs
weight: 80
url: /ar/net/aspose.words.saving/imagesaveoptions/jpegquality/
---
## ImageSaveOptions.JpegQuality property

الحصول على أو تعيين قيمة تحدد جودة صور JPEG التي تم إنشاؤها.

```csharp
public int JpegQuality { get; set; }
```

## ملاحظات

يكون له تأثير فقط عند الحفظ إلى JPEG.

استخدم هذه الخاصية للحصول على جودة الصور التي تم إنشاؤها أو تعيينها عند الحفظ بتنسيق JPEG. قد تختلف القيمة من 0 إلى 100 حيث يعني 0 أسوأ جودة ولكن الحد الأقصى للضغط و100 يعني أفضل جودة ولكن الحد الأدنى من الضغط.

القيمة الافتراضية هي 95.

## أمثلة

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

* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
