---
title: Story.DeleteShapes
linktitle: DeleteShapes
articleTitle: DeleteShapes
second_title: Aspose.Words for .NET
description: Effortlessly remove all shapes from your story text with the DeleteShapes method. Simplify your content and enhance clarity today!
type: docs
weight: 70
url: /net/aspose.words/story/deleteshapes/
---
## Story.DeleteShapes method

Deletes all shapes from the text of this story.

```csharp
public void DeleteShapes()
```

## Examples

Shows how to remove all shapes from a node.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Use a DocumentBuilder to insert a shape. This is an inline shape,
// which has a parent Paragraph, which is a child node of the first section's Body.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.That(doc.GetChildNodes(NodeType.Shape, true).Count, Is.EqualTo(1));

// We can delete all shapes from the child paragraphs of this Body.
Assert.That(doc.FirstSection.Body.StoryType, Is.EqualTo(StoryType.MainText));
doc.FirstSection.Body.DeleteShapes();

Assert.That(doc.GetChildNodes(NodeType.Shape, true).Count, Is.EqualTo(0));
```

### See Also

* class [Story](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
