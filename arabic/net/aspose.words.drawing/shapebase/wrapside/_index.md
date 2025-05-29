---
title: ShapeBase.WrapSide
linktitle: WrapSide
articleTitle: WrapSide
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase WrapSide للتحكم في التفاف النص حول الأشكال، مما يعزز الجاذبية البصرية لتصميمك وسهولة قراءته.
type: docs
weight: 630
url: /ar/net/aspose.words.drawing/shapebase/wrapside/
---
## ShapeBase.WrapSide property

يحدد كيفية لف النص حول الشكل.

```csharp
public WrapSide WrapSide { get; set; }
```

## ملاحظات

القيمة الافتراضية هيBoth.

له تأثير فقط على الأشكال ذات المستوى الأعلى.

## أمثلة

يوضح كيفية استبدال كافة أشكال مربع النص بأشكال الصور.

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

* enum [WrapSide](../../wrapside/)
* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
