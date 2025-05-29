---
title: ShapeBase.FlipOrientation
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase FlipOrientation لتبديل اتجاه الشكل بسهولة، مما يعزز تصميماتك بسهولة وإبداع.
type: docs
weight: 180
url: /ar/net/aspose.words.drawing/shapebase/fliporientation/
---
## ShapeBase.FlipOrientation property

يقوم بتبديل اتجاه الشكل.

```csharp
public FlipOrientation FlipOrientation { get; set; }
```

## ملاحظات

القيمة الافتراضية هيNone.

## أمثلة

يوضح كيفية قلب الشكل على المحور.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج شكل صورة واترك اتجاهها في حالتها الافتراضية.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

Assert.AreEqual(FlipOrientation.None, shape.FlipOrientation);

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// اضبط خاصية "FlipOrientation" على "FlipOrientation.Horizontal" لقلب الشكل الثاني على المحور y،
//جعله صورة أفقية معكوسة للشكل الأول.
shape.FlipOrientation = FlipOrientation.Horizontal;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// اضبط خاصية "FlipOrientation" على "FlipOrientation.Horizontal" لقلب الشكل الثالث على المحور x،
//جعله صورة معكوسة عمودية للشكل الأول.
shape.FlipOrientation = FlipOrientation.Vertical;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// اضبط خاصية "FlipOrientation" على "FlipOrientation.Horizontal" لقلب الشكل الرابع على كل من المحورين x وy،
//جعله صورة معكوسة أفقية ورأسية للشكل الأول.
shape.FlipOrientation = FlipOrientation.Both;

doc.Save(ArtifactsDir + "Shape.FlipShapeOrientation.docx");
```

### أنظر أيضا

* enum [FlipOrientation](../../fliporientation/)
* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
