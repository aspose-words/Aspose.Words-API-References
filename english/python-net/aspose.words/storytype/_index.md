---
title: StoryType enumeration
linktitle: StoryType enumeration
articleTitle: StoryType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.StoryType enumeration. Text of a Word document is stored in stories"
type: docs
weight: 1120
url: /python-net/aspose.words/storytype/
---

## StoryType enumeration

Text of a Word document is stored in stories. [StoryType](./) identifies a story.



### Members

| Name | Description |
| --- | --- |
| NONE | Default value. There is no such story in the document. |
| MAIN_TEXT | Contains the main text of the document, represented by [Body](../body/). |
| FOOTNOTES | Contains footnote text, represented by [Footnote](../../aspose.words.notes/footnote/). |
| ENDNOTES | Contains endnotes text, represented by [Footnote](../../aspose.words.notes/footnote/). |
| COMMENTS | Contains document comments (annotations), represented by [Comment](../comment/). |
| TEXTBOX | Contains shape or textbox text, represented by [Shape](../../aspose.words.drawing/shape/). |
| EVEN_PAGES_HEADER | Contains text of the even pages header, represented by [HeaderFooter](../headerfooter/). |
| PRIMARY_HEADER | Contains text of the primary header. When header is different for odd and even pages, contains text of the odd pages header. Represented by [HeaderFooter](../headerfooter/). |
| EVEN_PAGES_FOOTER | Contains text of the even pages footer, represented by [HeaderFooter](../headerfooter/). |
| PRIMARY_FOOTER | Contains text of the primary footer. When footer is different for odd and even pages, contains text of the odd pages footer. Represented by [HeaderFooter](../headerfooter/). |
| FIRST_PAGE_HEADER | Contains text of the first page header, represented by [HeaderFooter](../headerfooter/). |
| FIRST_PAGE_FOOTER | Contains text of the first page footer, represented by [HeaderFooter](../headerfooter/). |
| FOOTNOTE_SEPARATOR | Contains the text of the footnote separator. |
| FOOTNOTE_CONTINUATION_SEPARATOR | Contains the text of the footnote continuation separator. |
| FOOTNOTE_CONTINUATION_NOTICE | Contains the text of the footnote continuation notice separator. |
| ENDNOTE_SEPARATOR | Contains the text of the endnote separator. |
| ENDNOTE_CONTINUATION_SEPARATOR | Contains the text of the endnote continuation separator. |
| ENDNOTE_CONTINUATION_NOTICE | Contains the text of the endnote continuation notice separator. |

### Examples

Shows how to remove all shapes from a node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Use a DocumentBuilder to insert a shape. This is an inline shape,
# which has a parent Paragraph, which is a child node of the first section's Body.
builder.insert_shape(shape_type=aw.drawing.ShapeType.CUBE, width=100, height=100)
self.assertEqual(1, doc.get_child_nodes(aw.NodeType.SHAPE, True).count)
# We can delete all shapes from the child paragraphs of this Body.
self.assertEqual(aw.StoryType.MAIN_TEXT, doc.first_section.body.story_type)
doc.first_section.body.delete_shapes()
self.assertEqual(0, doc.get_child_nodes(aw.NodeType.SHAPE, True).count)
```

### See Also

* module [aspose.words](../)

