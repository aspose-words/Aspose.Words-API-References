---
title: Story.StoryType
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words for .NET
description: Story StoryType property. Gets the type of this story in C#.
type: docs
weight: 40
url: /net/aspose.words/story/storytype/
---
## Story.StoryType property

Gets the type of this story.

```csharp
public StoryType StoryType { get; }
```

## Examples

Shows how to remove all shapes from a node.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Use a DocumentBuilder to insert a shape. This is an inline shape,
// which has a parent Paragraph, which is a child node of the first section's Body.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// We can delete all shapes from the child paragraphs of this Body.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### See Also

* enum [StoryType](../../storytype/)
* class [Story](../)
* namespace [Aspose.Words](../../story/)
* assembly [Aspose.Words](../../../)
