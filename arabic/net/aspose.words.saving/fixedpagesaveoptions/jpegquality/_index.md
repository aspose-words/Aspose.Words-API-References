---
title: FixedPageSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words لـ .NET
description: حسّن جودة JPEG في مستندات HTML باستخدام FixedPageSaveOptions. اضبط جودة Jpeg بسهولة للحصول على وضوح مذهل للصورة.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/fixedpagesaveoptions/jpegquality/
---
## FixedPageSaveOptions.JpegQuality property

يحصل على قيمة تحدد جودة صور JPEG داخل مستند HTML أو يعينها.

```csharp
public int JpegQuality { get; set; }
```

## ملاحظات

يكون له تأثير فقط عندما يحتوي المستند على صور JPEG.

استخدم هذه الخاصية للحصول على جودة الصور داخل المستند أو تعيينها عند الحفظ بتنسيق صفحة ثابتة. قد تختلف القيمة من 0 إلى 100 حيث يعني 0 أسوأ جودة ولكن الحد الأقصى للضغط ويعني 100 أفضل جودة ولكن الحد الأدنى للضغط.

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

* class [FixedPageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
