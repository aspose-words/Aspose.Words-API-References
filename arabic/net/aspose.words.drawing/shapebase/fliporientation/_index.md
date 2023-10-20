---
title: ShapeBase.FlipOrientation
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words لـ .NET
description: ShapeBase FlipOrientation ملكية. تبديل اتجاه الشكل في C#.
type: docs
weight: 180
url: /ar/net/aspose.words.drawing/shapebase/fliporientation/
---
## ShapeBase.FlipOrientation property

تبديل اتجاه الشكل.

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

// أدخل شكل صورة واترك اتجاهه في حالته الافتراضية.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

Assert.AreEqual(FlipOrientation.None, shape.FlipOrientation);

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// اضبط الخاصية "FlipOrientation" على "FlipOrientation.Horizontal" لقلب الشكل الثاني على المحور y،
// جعلها صورة معكوسة أفقية للشكل الأول.
shape.FlipOrientation = FlipOrientation.Horizontal;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// اضبط الخاصية "FlipOrientation" على "FlipOrientation.Horizontal" لقلب الشكل الثالث على المحور السيني،
// تحويلها إلى صورة معكوسة عمودية للشكل الأول.
shape.FlipOrientation = FlipOrientation.Vertical;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// اضبط الخاصية "FlipOrientation" على "FlipOrientation.Horizontal" لقلب الشكل الرابع على المحورين x وy،
// تحويلها إلى صورة مرآة أفقية ورأسية للشكل الأول.
shape.FlipOrientation = FlipOrientation.Both;

doc.Save(ArtifactsDir + "Shape.FlipShapeOrientation.docx");
```

### أنظر أيضا

* enum [FlipOrientation](../../fliporientation/)
* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
