---
title: NodeCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: 用于 .NET 的 Aspose.Words
description: NodeCollection ToArray 方法. 将集合中的所有节点复制到新的节点数组 在 C#.
type: docs
weight: 110
url: /zh/net/aspose.words/nodecollection/toarray/
---
## NodeCollection.ToArray method

将集合中的所有节点复制到新的节点数组。

```csharp
public Node[] ToArray()
```

### 返回值

节点数组。

## 评论

您不应在迭代节点集合 时添加/删除节点，因为这会使迭代器无效并且需要刷新实时集合。

为了能够在迭代期间添加/删除节点，请使用此方法将 节点复制到固定大小的数组中，然后迭代该数组。

## 例子

演示如何用图像形状替换所有文本框形状。

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

* class [Node](../../node/)
* class [NodeCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
