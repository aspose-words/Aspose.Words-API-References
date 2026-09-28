---
title: InlineStory.first_paragraph property
linktitle: first_paragraph property
articleTitle: first_paragraph property
second_title: Aspose.Words for Python
description: "InlineStory.first_paragraph property. Gets the first paragraph in the story."
type: docs
weight: 10
url: /zh/python-net/aspose.words/inlinestory/first_paragraph/
---

## InlineStory.first_paragraph property

Gets the first paragraph in the story.


```python
@property
def first_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to insert and customize footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 添加文本，并用脚注引用它。此脚注将在文本后放置一个小的上标引用
# 标记在它引用的文本之后，并在页面底部的正文下方创建一个条目。
# 此条目将包含脚注的引用标记和引用文本，
# 我们将把它传递给文档生成器的 "InsertFootnote" 方法。
builder.write('Main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# 如果此属性设置为 "true"，则我们的脚注引用标记
# 将是该章节所有脚注中的索引。
# 这是第一个脚注，因此引用标记将是 "1"。
self.assertTrue(footnote.is_auto)
# 我们可以将文档生成器移动到脚注内部以编辑其引用文本。
builder.move_to(footnote.first_paragraph)
builder.write(' More text added by a DocumentBuilder.')
builder.move_to_document_end()
self.assertEqual('\x02 Footnote text. More text added by a DocumentBuilder.', footnote.get_text().strip())
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# 我们可以设置自定义引用标记，脚注将使用它而不是其索引号。
footnote.reference_mark = 'RefMark'
self.assertFalse(footnote.is_auto)
# 即使将 "IsAuto" 标志设置为 true，书签仍会显示其真实索引
# 即使之前的书签显示自定义引用标记，这个书签的引用标记也将是 "3"。
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
self.assertTrue(footnote.is_auto)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.AddFootnote.docx')
```

Shows how to add a comment to a paragraph.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('Hello world!')
comment = aw.Comment(doc, 'John Doe', 'JD', date.today())
builder.current_paragraph.append_child(comment)
builder.move_to(comment.append_child(aw.Paragraph(doc)))
builder.write('Comment text.')
self.assertEqual(date.today(), comment.date_time.date())
# 在 Microsoft Word 中，我们可以右键单击文档正文中的此评论进行编辑，或回复它。
doc.save(ARTIFACTS_DIR + 'InlineStory.add_comment.docx')
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

