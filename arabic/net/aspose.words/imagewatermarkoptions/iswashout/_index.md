---
title: ImageWatermarkOptions.IsWashout
second_title: Aspose.Words لمراجع .NET API
description: ImageWatermarkOptions ملكية. الحصول على أو تعيين قيمة منطقية مسؤولة عن تأثير تبييض العلامة المائية. القيمة الافتراضية هيحقيقي .
type: docs
weight: 20
url: /ar/net/aspose.words/imagewatermarkoptions/iswashout/
---
## ImageWatermarkOptions.IsWashout property

الحصول على أو تعيين قيمة منطقية مسؤولة عن تأثير تبييض العلامة المائية. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool IsWashout { get; set; }
```

### أمثلة

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
* مساحة الاسم [Aspose.Words](../../imagewatermarkoptions/)
* المجسم [Aspose.Words](../../../)


