---
title: ImageSize.HorizontalResolution
linktitle: HorizontalResolution
articleTitle: HorizontalResolution
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ImageSize HorizontalResolution للحصول بسهولة على DPI للصور الخاصة بك، مما يعزز الجودة والدقة في مشاريعك.
type: docs
weight: 40
url: /ar/net/aspose.words.drawing/imagesize/horizontalresolution/
---
## ImageSize.HorizontalResolution property

يحصل على الدقة الأفقية بوحدة DPI.

```csharp
public double HorizontalResolution { get; }
```

## أمثلة

يوضح كيفية قراءة خصائص الصورة في الشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج شكل في المستند الذي يحتوي على صورة مأخوذة من نظام الملفات المحلي لدينا.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// إذا كان الشكل يحتوي على صورة، فإن خاصية ImageData الخاصة به ستكون صالحة،
//وسوف يحتوي على كائن ImageSize.
ImageSize imageSize = shape.ImageData.ImageSize;

// يحتوي كائن ImageSize على معلومات للقراءة فقط حول الصورة الموجودة داخل الشكل.
Assert.AreEqual(400, imageSize.HeightPixels);
Assert.AreEqual(400, imageSize.WidthPixels);

const double delta = 0.05;
Assert.AreEqual(95.98d, imageSize.HorizontalResolution, delta);
Assert.AreEqual(95.98d, imageSize.VerticalResolution, delta);

// يمكننا تحديد حجم الشكل بناءً على حجم صورته لتجنب تمدد الصورة.
shape.Width = imageSize.WidthPoints * 2;
shape.Height = imageSize.HeightPoints * 2;

doc.Save(ArtifactsDir + "Drawing.ImageSize.docx");
```

### أنظر أيضا

* class [ImageSize](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
