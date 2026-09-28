---
title: InlineStory.parent_paragraph property
linktitle: parent_paragraph property
articleTitle: parent_paragraph property
second_title: Aspose.Words for Python
description: "InlineStory.parent_paragraph property. Retrieves the parent [Paragraph](../../paragraph/) of this node."
type: docs
weight: 90
url: /zh/python-net/aspose.words/inlinestory/parent_paragraph/
---

## InlineStory.parent_paragraph property

Retrieves the parent [Paragraph](../../paragraph/) of this node.



```python
@property
def parent_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to insert InlineStory nodes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text=None)
# 表节点具有 "EnsureMinimum()" 方法，可确保表至少有一个单元格。
table = aw.tables.Table(doc)
table.ensure_minimum()
# 我们可以在脚注中放置表格，使其出现在引用页的页脚。
self.assertEqual(0, footnote.tables.count)
footnote.append_child(table)
self.assertEqual(1, footnote.tables.count)
self.assertEqual(aw.NodeType.TABLE, footnote.last_child.node_type)
# InlineStory 也有一个 "EnsureMinimum()" 方法，但在这种情况下，
# 它确保节点的最后一个子节点是段落，
# 以便我们能够在 Microsoft Word 中轻松点击并编写文本。
footnote.ensure_minimum()
self.assertEqual(aw.NodeType.PARAGRAPH, footnote.last_child.node_type)
# 编辑锚点的外观，即小的上标数字
# 在指向脚注的正文中。
footnote.font.name = 'Arial'
footnote.font.color = aspose.pydrawing.Color.green
# 所有内联故事节点都有各自的故事类型。
self.assertEqual(aw.StoryType.FOOTNOTES, footnote.story_type)
# 注释是另一种内联故事。
comment = builder.current_paragraph.append_child(aw.Comment(doc=doc, author='John Doe', initial='J. D.', date_time=datetime.datetime.now())).as_comment()
# 内联故事节点的父段落将是主文档正文中的段落。
self.assertEqual(doc.first_section.body.first_paragraph, comment.parent_paragraph)
# 然而，最后一个段落是来自注释文本内容的段落，
# 它将位于主文档正文之外的气泡中。
# 默认情况下，注释不会有任何子节点，
# 因此我们可以应用 EnsureMinimum() 方法在此处也放置一个段落。
self.assertIsNone(comment.last_paragraph)
comment.ensure_minimum()
self.assertEqual(aw.NodeType.PARAGRAPH, comment.last_child.node_type)
# 一旦我们有了段落，就可以移动构建器来执行此操作并编写我们的注释。
builder.move_to(comment.last_paragraph)
builder.write('My comment.')
self.assertEqual(aw.StoryType.COMMENTS, comment.story_type)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.InsertInlineStoryNodes.docx')
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

