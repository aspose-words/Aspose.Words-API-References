---
title: WrapSide Enum
linktitle: WrapSide
articleTitle: WrapSide
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.WrapSide 枚举来控制环绕形状和图像的文本，增强文档布局和可读性。
type: docs
weight: 1800
url: /zh/net/aspose.words.drawing/wrapside/
---
## WrapSide enumeration

指定文本环绕形状或图片的哪一侧。

```csharp
public enum WrapSide
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Both | `0` | 文档文本在形状的两侧换行。 |
| Left | `1` | 文档文本仅在形状左侧换行。形状右侧有一个无文本区域。 |
| Right | `2` | 文档文本仅在形状右侧换行。形状左侧有一个无文本区域。 |
| Largest | `3` | 文档文本在形状距离页边距最远的一侧换行，在形状的另一侧留下空白区域。 |
| Default | `0` | 默认值为Both. |

## 例子

展示如何用图像形状替换所有文本框形状。

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

### 也可以看看

* property [WrapSide](../shapebase/wrapside/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
