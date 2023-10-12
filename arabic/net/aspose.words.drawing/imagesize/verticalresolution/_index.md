---
title: ImageSize.VerticalResolution
second_title: Aspose.Words لمراجع .NET API
description: ImageSize ملكية. الحصول على الدقة الرأسية بـ DPI.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing/imagesize/verticalresolution/
---
## ImageSize.VerticalResolution property

الحصول على الدقة الرأسية بـ DPI.

```csharp
public double VerticalResolution { get; }
```

### أمثلة

يوضح كيفية قراءة خصائص الصورة في الشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل شكلاً في المستند الذي يحتوي على صورة مأخوذة من نظام الملفات المحلي لدينا.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// إذا كان الشكل يحتوي على صورة، فستكون خاصية ImageData الخاصة به صالحة،
// وسيحتوي على كائن ImageSize.
ImageSize imageSize = shape.ImageData.ImageSize; 

// يحتوي كائن ImageSize على معلومات للقراءة فقط حول الصورة داخل الشكل.
Assert.AreEqual(400, imageSize.HeightPixels);
Assert.AreEqual(400, imageSize.WidthPixels);

const double delta = 0.05;
Assert.AreEqual(95.98d, imageSize.HorizontalResolution, delta);
Assert.AreEqual(95.98d, imageSize.VerticalResolution, delta);

// يمكننا أن نبني حجم الشكل على حجم صورته لتجنب تمديد الصورة.
shape.Width = imageSize.WidthPoints * 2;
shape.Height = imageSize.HeightPoints * 2;

doc.Save(ArtifactsDir + "Drawing.ImageSize.docx");
```

### أنظر أيضا

* class [ImageSize](../)
* مساحة الاسم [Aspose.Words.Drawing](../../imagesize/)
* المجسم [Aspose.Words](../../../)


