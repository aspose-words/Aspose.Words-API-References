---
title: ImageWatermarkOptions.Scale
linktitle: Scale
articleTitle: Scale
second_title: Aspose.Words لـ .NET
description: ImageWatermarkOptions Scale ملكية. الحصول على أو تعيين عامل القياس المعبر عنه بجزء صغير من الصورة. القيمة الافتراضية هي 0  auto في C#.
type: docs
weight: 30
url: /ar/net/aspose.words/imagewatermarkoptions/scale/
---
## ImageWatermarkOptions.Scale property

الحصول على أو تعيين عامل القياس المعبر عنه بجزء صغير من الصورة. القيمة الافتراضية هي 0 - auto.

```csharp
public double Scale { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentOutOfRangeException | يتم طرحه عندما تكون الوسيطة خارج نطاق القيم الصالحة. |

## ملاحظات

تتراوح القيم الصالحة من 0 إلى 65.5 ضمناً.

يعني المقياس التلقائي أنه سيتم تغيير حجم العلامة المائية إلى الحد الأقصى للعرض والحد الأقصى للارتفاع بالنسبة إلى هوامش الصفحة.

## أمثلة

يوضح كيفية إنشاء علامة مائية من صورة في نظام الملفات المحلي.

```csharp
Document doc = new Document();

            // تعديل مظهر العلامة المائية للصورة باستخدام كائن ImageWatermarkOptions،
            // ثم قم بتمريرها أثناء إنشاء علامة مائية من ملف صورة.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET48 || JAVA
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);
#elif NET5_0_OR_GREATER || __MOBILE__
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
