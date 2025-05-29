---
title: ImageSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words لـ .NET
description: اضبط خاصية جودة Jpeg في خيارات حفظ الصورة لتحسين جودة صورة JPEG، للحصول على صور مذهلة وأداء مُحسّن. مثالي للمطورين!
type: docs
weight: 80
url: /ar/net/aspose.words.saving/imagesaveoptions/jpegquality/
---
## ImageSaveOptions.JpegQuality property

يحصل على قيمة تحدد جودة صور JPEG المولدة أو يعينها.

```csharp
public int JpegQuality { get; set; }
```

## ملاحظات

لا يكون له تأثير إلا عند الحفظ بتنسيق JPEG.

استخدم هذه الخاصية للحصول على جودة الصور المولدة أو تعيينها عند الحفظ بتنسيق JPEG. قد تختلف القيمة من 0 إلى 100 حيث يعني 0 أسوأ جودة ولكن الحد الأقصى للضغط ويعني 100 أفضل جودة ولكن الحد الأدنى للضغط.

القيمة الافتراضية هي 95.

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

* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
