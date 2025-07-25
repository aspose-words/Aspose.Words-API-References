---
title: Story.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words for .NET
description: Access the last paragraph of your story effortlessly with the Story LastParagraph property, enhancing your narrative management and editing experience.
type: docs
weight: 20
url: /net/aspose.words/story/lastparagraph/
---
## Story.LastParagraph property

Gets the last paragraph in the story.

```csharp
public Paragraph LastParagraph { get; }
```

## Examples

Shows how to move a DocumentBuilder's cursor position to a specified node.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// The document builder has a cursor, which acts as the part of the document
// where the builder appends new nodes when we use its document construction methods.
// This cursor functions in the same way as Microsoft Word's blinking cursor,
// and it also always ends up immediately after any node that the builder just inserted.
// To append content to a different part of the document,
// we can move the cursor to a different node with the "MoveTo" method.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// The cursor is now in front of the node that we moved it to.
// Adding a second run will insert it in front of the first run.
builder.Writeln("Run 2. ");

Assert.That(doc.GetText().Trim(), Is.EqualTo("Run 2. \rRun 1."));

// Move the cursor to the end of the document to continue appending text to the end as before.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.That(doc.GetText().Trim(), Is.EqualTo("Run 2. \rRun 1. \rRun 3."));
```

### See Also

* class [Paragraph](../../paragraph/)
* class [Story](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
