---
title: FlipOrientation Enum
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Drawing.FlipOrientation enum لخيارات توجيه متعددة للأشكال. حسّن تصميم مستندك بتخصيص مرن!
type: docs
weight: 1290
url: /ar/net/aspose.words.drawing/fliporientation/
---
## FlipOrientation enumeration

القيم الممكنة لاتجاه الشكل.

```csharp
[Flags]
public enum FlipOrientation
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لا يتم قلب الإحداثيات. |
| Horizontal | `1` | انقلب على طول المحور y، مع عكس إحداثيات x. |
| Vertical | `2` | انقلب على طول المحور السيني، مع عكس إحداثيات y. |
| Both | `3` | انقلب على طول المحورين y وx. |

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

* property [FlipOrientation](../shapebase/fliporientation/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
