---
title: DocumentBuilder.CurrentStory
linktitle: CurrentStory
articleTitle: CurrentStory
second_title: Aspose.Words for .NET
description: Discover the DocumentBuilder CurrentStory property to access and manage the selected story efficiently, enhancing your document editing experience.
type: docs
weight: 70
url: /net/aspose.words/documentbuilder/currentstory/
---
## DocumentBuilder.CurrentStory property

Gets the story that is currently selected in this [`DocumentBuilder`](../).

```csharp
public Story CurrentStory { get; }
```

## Examples

Shows how to work with a document builder's current story.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A Story is a type of node that has child Paragraph nodes, such as a Body.
Assert.That(doc.FirstSection.Body, Is.EqualTo(builder.CurrentStory));
Assert.That(builder.CurrentParagraph.ParentNode, Is.EqualTo(builder.CurrentStory));
Assert.That(builder.CurrentStory.StoryType, Is.EqualTo(StoryType.MainText));

builder.CurrentStory.AppendParagraph("Text added to current Story.");

// A Story can also contain tables.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1");
builder.InsertCell();
builder.Write("Row 1, cell 2");
builder.EndTable();

Assert.That(builder.CurrentStory.Tables.Contains(table), Is.True);
```

### See Also

* class [Story](../../story/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
