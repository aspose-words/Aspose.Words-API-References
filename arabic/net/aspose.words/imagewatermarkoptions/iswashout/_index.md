---
title: ImageWatermarkOptions.IsWashout
linktitle: IsWashout
articleTitle: IsWashout
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية IsWashout في ImageWatermarkOptions. تحكم في تأثير إزالة العلامة المائية بسهولة باستخدام هذا الإعداد المنطقي البسيط.
type: docs
weight: 20
url: /ar/net/aspose.words/imagewatermarkoptions/iswashout/
---
## ImageWatermarkOptions.IsWashout property

يحصل على قيمة منطقية أو يعينها وهي المسؤولة عن تأثير غسل العلامة المائية. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool IsWashout { get; set; }
```

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

* class [ImageWatermarkOptions](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
