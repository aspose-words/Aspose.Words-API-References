---
title: WrapSide Enum
linktitle: WrapSide
articleTitle: WrapSide
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.WrapSide تعداد. يحدد الجانب الجوانب من الشكل أو الصورة الذي يلتف النص حوله في C#.
type: docs
weight: 1390
url: /ar/net/aspose.words.drawing/wrapside/
---
## WrapSide enumeration

يحدد الجانب (الجوانب) من الشكل أو الصورة الذي يلتف النص حوله.

```csharp
public enum WrapSide
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Both | `0` | يلتف نص المستند على جانبي الشكل. |
| Left | `1` | يلتف نص المستند على الجانب الأيسر من الشكل فقط. توجد منطقة خالية من النص على يمين الشكل. |
| Right | `2` | يلتف نص المستند على الجانب الأيمن من الشكل فقط. توجد منطقة خالية من النص على الجانب الأيسر من الشكل. |
| Largest | `3` | يلتف نص المستند على جانب الشكل الأبعد عن هامش الصفحة، مما يترك مساحة خالية من النص على الجانب الآخر من الشكل. |
| Default | `0` | القيمة الافتراضية هيBoth . |

## أمثلة

يوضح كيفية استبدال جميع أشكال مربعات النص بأشكال الصور.

```csharp
Document doc = new Document(MyDir + "Textboxes in drawing canvas.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(3, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(1, shapes.Count(s => s.ShapeType == ShapeType.Image));

foreach (Shape shape in shapes)
{
    if (shape.ShapeType == ShapeType.TextBox)
    {
        Shape replacementShape = new Shape(doc, ShapeType.Image);
        replacementShape.ImageData.SetImage(ImageDir + "Logo.jpg");
        replacementShape.Left = shape.Left;
        replacementShape.Top = shape.Top;
        replacementShape.Width = shape.Width;
        replacementShape.Height = shape.Height;
        replacementShape.RelativeHorizontalPosition = shape.RelativeHorizontalPosition;
        replacementShape.RelativeVerticalPosition = shape.RelativeVerticalPosition;
        replacementShape.HorizontalAlignment = shape.HorizontalAlignment;
        replacementShape.VerticalAlignment = shape.VerticalAlignment;
        replacementShape.WrapType = shape.WrapType;
        replacementShape.WrapSide = shape.WrapSide;

        shape.ParentNode.InsertAfter(replacementShape, shape);
        shape.Remove();
    }
}

shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(0, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(4, shapes.Count(s => s.ShapeType == ShapeType.Image));

doc.Save(ArtifactsDir + "Shape.ReplaceTextboxesWithImages.docx");
```

### أنظر أيضا

* property [WrapSide](../shapebase/wrapside/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
