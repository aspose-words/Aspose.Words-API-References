---
title: ImageWatermarkOptions Class
linktitle: ImageWatermarkOptions
articleTitle: ImageWatermarkOptions
second_title: Aspose.Words لـ .NET
description: اكتشف خيارات Aspose.Words.ImageWatermark. خصّص علاماتك المائية على صورك بسهولة مع خيارات متعددة لعرض مستنداتك بشكل محسّن.
type: docs
weight: 3670
url: /ar/net/aspose.words/imagewatermarkoptions/
---
## ImageWatermarkOptions class

يحتوي على خيارات يمكن تحديدها عند إضافة علامة مائية مع الصورة.

لمعرفة المزيد، قم بزيارة[العمل مع العلامة المائية](https://docs.aspose.com/words/net/working-with-watermark/) مقالة توثيقية.

```csharp
public class ImageWatermarkOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [ImageWatermarkOptions](imagewatermarkoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [IsWashout](../../aspose.words/imagewatermarkoptions/iswashout/) { get; set; } | يحصل على قيمة منطقية أو يعينها وهي المسؤولة عن تأثير غسل العلامة المائية. القيمة الافتراضية هي`حقيقي` . |
| [Scale](../../aspose.words/imagewatermarkoptions/scale/) { get; set; } | يحصل على أو يضبط عامل المقياس المعبر عنه كنسبة مئوية من الصورة. القيمة الافتراضية هي 0 - تلقائي. |

## أمثلة

يوضح كيفية إنشاء علامة مائية من صورة في نظام الملفات المحلي.

```csharp
Document doc = new Document();

            // تعديل مظهر العلامة المائية للصورة باستخدام كائن ImageWatermarkOptions،
            // ثم مررها أثناء إنشاء علامة مائية من ملف صورة.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // لدينا خيارات مختلفة لإدراج الصورة:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
