---
title: NodeCollection Class
linktitle: NodeCollection
articleTitle: NodeCollection
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.NodeCollection class, your go-to solution for managing diverse node types efficiently in document processing. Enhance your workflow today!
type: docs
weight: 4880
url: /net/aspose.words/nodecollection/
---
## NodeCollection class

Represents a collection of nodes of a specific type.

To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) documentation article.

```csharp
public class NodeCollection : IEnumerable<Node>
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Gets the number of nodes in the collection. |
| [Item](../../aspose.words/nodecollection/item/) { get; } | Retrieves a node at the given index. |

## Methods

| Name | Description |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Adds a node to the end of the collection. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Removes all nodes from this collection and from the document. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Determines whether a node is in the collection. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Provides a simple "foreach" style iteration over the collection of nodes. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Returns the zero-based index of the specified node. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Inserts a node into the collection at the specified index. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Removes the node from the collection and from the document. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Removes the node at the specified index from the collection and from the document. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Copies all nodes from the collection to a new array of nodes. |

## Remarks

`NodeCollection` does not own the nodes it contains, rather, is just a selection of nodes of the specified type, but the nodes are stored in the tree under their respective parent nodes.

`NodeCollection` supports indexed access, iteration and provides add and remove methods.

The `NodeCollection` collection is "live", i.e. changes to the children of the node object that it was created from are immediately reflected in the nodes returned by the `NodeCollection` properties and methods.

`NodeCollection` is returned by [`GetChildNodes`](../compositenode/getchildnodes/) and also serves as a base class for typed node collections such as [`SectionCollection`](../sectioncollection/), [`ParagraphCollection`](../paragraphcollection/) etc.

`NodeCollection` can be "flat" and contain only immediate children of the node it was created from, or it can be "deep" and contain all descendant children.

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

* class [Node](../node/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
