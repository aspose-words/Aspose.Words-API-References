---
title: ImageWatermarkOptions.Scale
linktitle: Scale
articleTitle: Scale
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ImageWatermarkOptions Scale لضبط مقياس الصورة بسهولة للحصول على علامة مائية مثالية. القيمة الافتراضية هي 0 تلقائي لضمان تكامل سلس.
type: docs
weight: 30
url: /ar/net/aspose.words/imagewatermarkoptions/scale/
---
## ImageWatermarkOptions.Scale property

يحصل على أو يضبط عامل المقياس المعبر عنه كنسبة مئوية من الصورة. القيمة الافتراضية هي 0 - تلقائي.

```csharp
public double Scale { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentOutOfRangeException | يتم طرحه عندما تكون الحجة خارج نطاق القيم الصالحة. |

## ملاحظات

تتراوح القيم الصالحة من 0 إلى 65.5 شاملة.

يعني المقياس التلقائي أن العلامة المائية سيتم قياسها إلى أقصى عرض وأقصى ارتفاع بالنسبة إلى هوامش الصفحة.

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
