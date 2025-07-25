---
title: InlineStory.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words for .NET
description: Discover the InlineStory Font property for seamless font formatting of anchor characters, enhancing your design with unique typography options.
type: docs
weight: 20
url: /net/aspose.words/inlinestory/font/
---
## InlineStory.Font property

Provides access to the font formatting of the anchor character of this object.

```csharp
public Font Font { get; }
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
Assert.That(footnote.Tables.Count, Is.EqualTo(0));
footnote.AppendChild(table);
Assert.That(footnote.Tables.Count, Is.EqualTo(1));
Assert.That(footnote.LastChild.NodeType, Is.EqualTo(NodeType.Table));

// An InlineStory has an "EnsureMinimum()" method as well, but in this case,
// it makes sure the last child of the node is a paragraph,
// for us to be able to click and write text easily in Microsoft Word.
footnote.EnsureMinimum();
Assert.That(footnote.LastChild.NodeType, Is.EqualTo(NodeType.Paragraph));

// Edit the appearance of the anchor, which is the small superscript number
// in the main text that points to the footnote.
footnote.Font.Name = "Arial";
footnote.Font.Color = Color.Green;

// All inline story nodes have their respective story types.
Assert.That(footnote.StoryType, Is.EqualTo(StoryType.Footnotes));

// A comment is another type of inline story.
Comment comment = (Comment)builder.CurrentParagraph.AppendChild(new Comment(doc, "John Doe", "J. D.", DateTime.Now));

// The parent paragraph of an inline story node will be the one from the main document body.
Assert.That(comment.ParentParagraph, Is.EqualTo(doc.FirstSection.Body.FirstParagraph));

// However, the last paragraph is the one from the comment text contents,
// which will be outside the main document body in a speech bubble.
// A comment will not have any child nodes by default,
// so we can apply the EnsureMinimum() method to place a paragraph here as well.
Assert.That(comment.LastParagraph, Is.Null);
comment.EnsureMinimum();
Assert.That(comment.LastChild.NodeType, Is.EqualTo(NodeType.Paragraph));

// Once we have a paragraph, we can move the builder to do it and write our comment.
builder.MoveTo(comment.LastParagraph);
builder.Write("My comment.");

Assert.That(comment.StoryType, Is.EqualTo(StoryType.Comments));

doc.Save(ArtifactsDir + "InlineStory.InsertInlineStoryNodes.docx");
```

### See Also

* class [Font](../../font/)
* class [InlineStory](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
