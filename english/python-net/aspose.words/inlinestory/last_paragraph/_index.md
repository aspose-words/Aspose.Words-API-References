---
title: last_paragraph property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets the last paragraph in the story."
type: docs
weight: 70
url: /python-net/aspose.words/inlinestory/last_paragraph/
---

## InlineStory.last_paragraph property

Gets the last paragraph in the story.


### Examples

Shows how to insert InlineStory nodes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
footnote = builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, None)

# Table nodes have an "ensure_minimum()" method that makes sure the table has at least one cell.
table = aw.tables.Table(doc)
table.ensure_minimum()

# We can place a table inside a footnote, which will make it appear at the referencing page's footer.
self.assertEqual(0, footnote.tables.count)
footnote.append_child(table)
self.assertEqual(1, footnote.tables.count)
self.assertEqual(aw.NodeType.TABLE, footnote.last_child.node_type)

# An InlineStory has an "ensure_minimum()" method as well, but in this case,
# it makes sure the last child of the node is a paragraph,
# for us to be able to click and write text easily in Microsoft Word.
footnote.ensure_minimum()
self.assertEqual(aw.NodeType.PARAGRAPH, footnote.last_child.node_type)

# Edit the appearance of the anchor, which is the small superscript number
# in the main text that points to the footnote.
footnote.font.name = "Arial"
footnote.font.color = drawing.Color.green

# All inline story nodes have their respective story types.
self.assertEqual(aw.StoryType.FOOTNOTES, footnote.story_type)

# A comment is another type of inline story.
comment = builder.current_paragraph.append_child(aw.Comment(doc, "John Doe", "J. D.", datetime.now())).as_comment()

# The parent paragraph of an inline story node will be the one from the main document body.
self.assertEqual(doc.first_section.body.first_paragraph, comment.parent_paragraph)

# However, the last paragraph is the one from the comment text contents,
# which will be outside the main document body in a speech bubble.
# A comment will not have any child nodes by default,
# so we can apply the ensure_minimum() method to place a paragraph here as well.
self.assertIsNone(comment.last_paragraph)
comment.ensure_minimum()
self.assertEqual(aw.NodeType.PARAGRAPH, comment.last_child.node_type)

# Once we have a paragraph, we can move the builder to do it and write our comment.
builder.move_to(comment.last_paragraph)
builder.write("My comment.")

self.assertEqual(aw.StoryType.COMMENTS, comment.story_type)

doc.save(ARTIFACTS_DIR + "InlineStory.insert_inline_story_nodes.docx")
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

