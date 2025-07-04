---
title: NodeCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words for .NET
description: Discover the NodeCollection ToArray method, effortlessly convert your node collection into a new array, enhancing data management and accessibility.
type: docs
weight: 110
url: /net/aspose.words/nodecollection/toarray/
---
## NodeCollection.ToArray method

Copies all nodes from the collection to a new array of nodes.

```csharp
public Node[] ToArray()
```

### Return Value

An array of nodes.

## Remarks

You should not be adding/removing nodes while iterating over a collection of nodes because it invalidates the iterator and requires refreshes for live collections.

To be able to add/remove nodes during iteration, use this method to copy nodes into a fixed-size array and then iterate over the array.

## Examples

Shows how to replace all textbox shapes with image shapes.

```csharp
Document doc = new Document(MyDir + "Textboxes in drawing canvas.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.That(shapes.Count(s => s.ShapeType == ShapeType.TextBox), Is.EqualTo(3));
Assert.That(shapes.Count(s => s.ShapeType == ShapeType.Image), Is.EqualTo(1));

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

Assert.That(shapes.Count(s => s.ShapeType == ShapeType.TextBox), Is.EqualTo(0));
Assert.That(shapes.Count(s => s.ShapeType == ShapeType.Image), Is.EqualTo(4));

doc.Save(ArtifactsDir + "Shape.ReplaceTextboxesWithImages.docx");
```

### See Also

* class [Node](../../node/)
* class [NodeCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
