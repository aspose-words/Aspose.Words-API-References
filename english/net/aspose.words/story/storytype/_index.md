---
title: Story.StoryType
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words for .NET
description: Discover the StoryType property to easily identify and categorize your stories, enhancing organization and improving your storytelling experience.
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

Assert.That(doc.GetChildNodes(NodeType.Shape, true).Count, Is.EqualTo(1));

// We can delete all shapes from the child paragraphs of this Body.
Assert.That(doc.FirstSection.Body.StoryType, Is.EqualTo(StoryType.MainText));
doc.FirstSection.Body.DeleteShapes();

Assert.That(doc.GetChildNodes(NodeType.Shape, true).Count, Is.EqualTo(0));
```

### See Also

* enum [StoryType](../../storytype/)
* class [Story](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
