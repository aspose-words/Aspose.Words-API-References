---
title: FlipOrientation Enum
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.FlipOrientation تعداد. القيم المحتملة لاتجاه الشكل في C#.
type: docs
weight: 970
url: /ar/net/aspose.words.drawing/fliporientation/
---
## FlipOrientation enumeration

القيم المحتملة لاتجاه الشكل.

```csharp
[Flags]
public enum FlipOrientation
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لم يتم قلب الإحداثيات. |
| Horizontal | `1` | اقلب على طول المحور y، مع عكس إحداثيات x. |
| Vertical | `2` | اقلب على طول المحور x، مع عكس إحداثيات y. |
| Both | `3` | اقلب على طول المحورين y وx. |

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

* property [FlipOrientation](../shapebase/fliporientation/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
