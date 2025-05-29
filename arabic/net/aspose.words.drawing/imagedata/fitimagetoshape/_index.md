---
title: ImageData.FitImageToShape
linktitle: FitImageToShape
articleTitle: FitImageToShape
second_title: Aspose.Words لـ .NET
description: قم بتحسين صورك باستخدام طريقة FitImageToShape، مما يضمن محاذاة نسبة العرض إلى الارتفاع المثالية داخل إطارات Shape للحصول على عروض مرئية مذهلة.
type: docs
weight: 190
url: /ar/net/aspose.words.drawing/imagedata/fitimagetoshape/
---
## ImageData.FitImageToShape method

تناسب بيانات الصورة مع إطار الشكل بحيث تتطابق نسبة العرض إلى الارتفاع لبيانات الصورة مع نسبة العرض إلى الارتفاع لإطار الشكل.

```csharp
public void FitImageToShape()
```

## أمثلة

يظهر ساخنًا لتناسب بيانات الصورة مع إطار الشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج شكل صورة واترك اتجاهها في حالتها الافتراضية.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 300, 450);
shape.ImageData.SetImage(ImageDir + "Barcode.png");
shape.ImageData.FitImageToShape();

doc.Save(ArtifactsDir + "Shape.FitImageToShape.docx");
```

### أنظر أيضا

* class [ImageData](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
