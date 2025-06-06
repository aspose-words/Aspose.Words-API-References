---
title: InlineStory.StoryType
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words for .NET
description: Discover the InlineStory StoryType property, which reveals the unique type of your story. Enhance your storytelling with precise categorization!
type: docs
weight: 100
url: /net/aspose.words/inlinestory/storytype/
---
## InlineStory.StoryType property

Returns the type of the story.

```csharp
public abstract StoryType StoryType { get; }
```

## Examples

Shows how to insert InlineStory nodes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, null);

// Table nodes have an "EnsureMinimum()" method that makes sure the table has at least one cell.
Table table = new Table(doc);
table.EnsureMinimum();

// We can place a table inside a footnote, which will make it appear at the referencing page's footer.
Assert.AreEqual(0, footnote.Tables.Count);
footnote.AppendChild(table);
Assert.AreEqual(1, footnote.Tables.Count);
Assert.AreEqual(NodeType.Table, footnote.LastChild.NodeType);

// An InlineStory has an "EnsureMinimum()" method as well, but in this case,
// it makes sure the last child of the node is a paragraph,
// for us to be able to click and write text easily in Microsoft Word.
footnote.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, footnote.LastChild.NodeType);

// Edit the appearance of the anchor, which is the small superscript number
// in the main text that points to the footnote.
footnote.Font.Name = "Arial";
footnote.Font.Color = Color.Green;

// All inline story nodes have their respective story types.
Assert.AreEqual(StoryType.Footnotes, footnote.StoryType);

// A comment is another type of inline story.
Comment comment = (Comment)builder.CurrentParagraph.AppendChild(new Comment(doc, "John Doe", "J. D.", DateTime.Now));

// The parent paragraph of an inline story node will be the one from the main document body.
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, comment.ParentParagraph);

// However, the last paragraph is the one from the comment text contents,
// which will be outside the main document body in a speech bubble.
// A comment will not have any child nodes by default,
// so we can apply the EnsureMinimum() method to place a paragraph here as well.
Assert.Null(comment.LastParagraph);
comment.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, comment.LastChild.NodeType);

// Once we have a paragraph, we can move the builder to do it and write our comment.
builder.MoveTo(comment.LastParagraph);
builder.Write("My comment.");

Assert.AreEqual(StoryType.Comments, comment.StoryType);

doc.Save(ArtifactsDir + "InlineStory.InsertInlineStoryNodes.docx");
```

### See Also

* enum [StoryType](../../storytype/)
* class [InlineStory](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
