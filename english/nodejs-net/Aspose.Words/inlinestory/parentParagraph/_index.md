---
title: InlineStory.parentParagraph property
linktitle: parentParagraph property
articleTitle: parentParagraph property
second_title: Aspose.Words for NodeJs
description: "InlineStory.parentParagraph property. Retrieves the parent [Paragraph](../../paragraph/) of this node."
type: docs
weight: 90
url: /nodejs-net/aspose.words/inlinestory/parentParagraph/
---

## InlineStory.parentParagraph property

Retrieves the parent [Paragraph](../../paragraph/) of this node.



```js
get parentParagraph(): Aspose.Words.Paragraph
```

### Examples

Shows how to insert InlineStory nodes.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
let footnote = builder.insertFootnote(aw.Notes.FootnoteType.Footnote, null);

// Table nodes have an "EnsureMinimum()" method that makes sure the table has at least one cell.
let table = new aw.Tables.Table(doc);
table.ensureMinimum();

// We can place a table inside a footnote, which will make it appear at the referencing page's footer.
expect(footnote.tables.count).toEqual(0);
footnote.appendChild(table);
expect(footnote.tables.count).toEqual(1);
expect(footnote.lastChild.nodeType).toEqual(aw.NodeType.Table);

// An InlineStory has an "EnsureMinimum()" method as well, but in this case,
// it makes sure the last child of the node is a paragraph,
// for us to be able to click and write text easily in Microsoft Word.
footnote.ensureMinimum();
expect(footnote.lastChild.nodeType).toEqual(aw.NodeType.Paragraph);

// Edit the appearance of the anchor, which is the small superscript number
// in the main text that points to the footnote.
footnote.font.name = "Arial";
footnote.font.color = "#008000";

// All inline story nodes have their respective story types.
expect(footnote.storyType).toEqual(aw.StoryType.Footnotes);

// A comment is another type of inline story.
let comment = builder.currentParagraph.appendChild(new aw.Comment(doc, "John Doe", "J. D.", Date.now())).asComment();

// The parent paragraph of an inline story node will be the one from the main document body.
expect(comment.parentParagraph.referenceEquals(doc.firstSection.body.firstParagraph)).toEqual(true);

// However, the last paragraph is the one from the comment text contents,
// which will be outside the main document body in a speech bubble.
// A comment will not have any child nodes by default,
// so we can apply the EnsureMinimum() method to place a paragraph here as well.
expect(comment.lastParagraph).toBe(null);
comment.ensureMinimum();
expect(comment.lastChild.nodeType).toEqual(aw.NodeType.Paragraph);

// Once we have a paragraph, we can move the builder to do it and write our comment.
builder.moveTo(comment.lastParagraph);
builder.write("My comment.");

expect(comment.storyType).toEqual(aw.StoryType.Comments);

doc.save(base.artifactsDir + "InlineStory.InsertInlineStoryNodes.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [InlineStory](../)

