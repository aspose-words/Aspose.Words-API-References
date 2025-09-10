---
title: StoryType enumeration
linktitle: StoryType enumeration
articleTitle: StoryType enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.StoryType enumeration. Text of a Word document is stored in stories"
type: docs
weight: 1250
url: /nodejs-net/aspose.words/storytype/
---

## StoryType enumeration

Text of a Word document is stored in stories. [StoryType](./) identifies a story.



### Members

| Name | Description |
| --- | --- |
| None | Default value. There is no such story in the document. |
| MainText | Contains the main text of the document, represented by [Body](../body/). |
| Footnotes | Contains footnote text, represented by [Footnote](../../aspose.words.notes/footnote/). |
| Endnotes | Contains endnotes text, represented by [Footnote](../../aspose.words.notes/footnote/). |
| Comments | Contains document comments (annotations), represented by [Comment](../comment/). |
| Textbox | Contains shape or textbox text, represented by [Shape](../../aspose.words.drawing/shape/). |
| EvenPagesHeader | Contains text of the even pages header, represented by [HeaderFooter](../headerfooter/). |
| PrimaryHeader | Contains text of the primary header. When header is different for odd and even pages, contains text of the odd pages header. Represented by [HeaderFooter](../headerfooter/). |
| EvenPagesFooter | Contains text of the even pages footer, represented by [HeaderFooter](../headerfooter/). |
| PrimaryFooter | Contains text of the primary footer. When footer is different for odd and even pages, contains text of the odd pages footer. Represented by [HeaderFooter](../headerfooter/). |
| FirstPageHeader | Contains text of the first page header, represented by [HeaderFooter](../headerfooter/). |
| FirstPageFooter | Contains text of the first page footer, represented by [HeaderFooter](../headerfooter/). |
| FootnoteSeparator | Contains the text of the footnote separator. |
| FootnoteContinuationSeparator | Contains the text of the footnote continuation separator. |
| FootnoteContinuationNotice | Contains the text of the footnote continuation notice separator. |
| EndnoteSeparator | Contains the text of the endnote separator. |
| EndnoteContinuationSeparator | Contains the text of the endnote continuation separator. |
| EndnoteContinuationNotice | Contains the text of the endnote continuation notice separator. |

### Examples

Shows how to remove all shapes from a node.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Use a DocumentBuilder to insert a shape. This is an inline shape,
// which has a parent Paragraph, which is a child node of the first section's Body.
builder.insertShape(aw.Drawing.ShapeType.Cube, 100.0, 100.0);

expect(doc.getChildNodes(aw.NodeType.Shape, true).count).toEqual(1);

// We can delete all shapes from the child paragraphs of this Body.
expect(doc.firstSection.body.storyType).toEqual(aw.StoryType.MainText);
doc.firstSection.body.deleteShapes();

expect(doc.getChildNodes(aw.NodeType.Shape, true).count).toEqual(0);
```

### See Also

* module [Aspose.Words](../)

