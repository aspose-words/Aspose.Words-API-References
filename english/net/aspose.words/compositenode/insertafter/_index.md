---
title: CompositeNode.InsertAfter
linktitle: InsertAfter
articleTitle: InsertAfter
second_title: Aspose.Words for .NET
description: Effortlessly insert nodes with the CompositeNode InsertAfter method, enhancing your data structure management and ensuring efficient node placement.
type: docs
weight: 150
url: /net/aspose.words/compositenode/insertafter/
---
## CompositeNode.InsertAfter&lt;T&gt; method

Inserts the specified node immediately after the specified reference node.

```csharp
public T InsertAfter<T>(T newChild, Node refChild)
    where T : Node
```

| Parameter | Type | Description |
| --- | --- | --- |
| newChild | T | The [`Node`](../../node/) to insert. |
| refChild | Node | The [`Node`](../../node/) that is the reference node. The *newChild* is placed after the *refChild*. |

### Return Value

The inserted node.

## Remarks

If *refChild* is `null`, inserts *newChild* at the beginning of the list of child nodes.

If the *newChild* is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use [`ImportNode`](../../documentbase/importnode/) to import the node to the current document. The imported node can then be inserted into the current document.

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

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```csharp
Document doc = new Document();

// An empty document, by default, has one paragraph.
Assert.That(doc.FirstSection.Body.Paragraphs.Count, Is.EqualTo(1));

// Composite nodes such as our paragraph can contain other composite and inline nodes as children.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Create three more run nodes.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// The document body will not display these runs until we insert them into a composite node
// that itself is a part of the document's node tree, as we did with the first run.
// We can determine where the text contents of nodes that we insert
// appears in the document by specifying an insertion location relative to another node in the paragraph.
Assert.That(paragraph.GetText().Trim(), Is.EqualTo("Initial text."));

// Insert the second run into the paragraph in front of the initial run.
paragraph.InsertBefore(run2, paragraphText);

Assert.That(paragraph.GetText().Trim(), Is.EqualTo("Run 2. Initial text."));

// Insert the third run after the initial run.
paragraph.InsertAfter(run3, paragraphText);

Assert.That(paragraph.GetText().Trim(), Is.EqualTo("Run 2. Initial text. Run 3."));

// Insert the first run to the start of the paragraph's child nodes collection.
paragraph.PrependChild(run1);

Assert.That(paragraph.GetText().Trim(), Is.EqualTo("Run 1. Run 2. Initial text. Run 3."));
Assert.That(paragraph.GetChildNodes(NodeType.Any, true).Count, Is.EqualTo(4));

// We can modify the contents of the run by editing and deleting existing child nodes.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.That(paragraph.GetText().Trim(), Is.EqualTo("Run 1. Updated run 2. Run 3."));
Assert.That(paragraph.GetChildNodes(NodeType.Any, true).Count, Is.EqualTo(3));
```

### See Also

* class [Node](../../node/)
* class [CompositeNode](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
