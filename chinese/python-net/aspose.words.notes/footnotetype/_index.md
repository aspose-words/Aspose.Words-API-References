---
title: FootnoteType enumeration
linktitle: FootnoteType enumeration
articleTitle: FootnoteType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnoteType enumeration. Specifies whether this is a footnote or an endnote."
type: docs
weight: 100
url: /zh/python-net/aspose.words.notes/footnotetype/
---

## FootnoteType enumeration

Specifies whether this is a footnote or an endnote.

Both footnotes and endnotes are represented by objects by the [FootnoteType.FOOTNOTE](./#FOOTNOTE)
class. Use [Footnote.footnote_type](../footnote/footnote_type/) to distinguish between footnotes 
and endnotes.




### Members

| Name | Description |
| --- | --- |
| FOOTNOTE | The object is a footnote. |
| ENDNOTE | The object is an endnote. |

### Examples

Shows how to reference text with a footnote and an endnote.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 插入一些文本并使用脚注标记它，默认情况下 IsAuto 属性设置为 "true"，
# 因此正文中看到的标记将自动编号为 "1"，
# 并且脚注将出现在页面底部。
builder.write('This text will be referenced by a footnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote comment regarding referenced text.')
# 插入更多文本并使用自定义引用标记的尾注标记它，
# 它将替代数字 "2" 使用，并将 "IsAuto" 设置为 false。
builder.write('This text will be referenced by an endnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote comment regarding referenced text.', reference_mark='CustomMark')
# 脚注始终出现在其引用文本的底部，
# 因此此分页符不会影响脚注。
# 另一方面，尾注始终位于文档的末尾
# 因此此分页符会将尾注推到下一页。
builder.insert_break(aw.BreakType.PAGE_BREAK)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertFootnote.docx')
```

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

### See Also

* module [aspose.words.notes](../)
* enum value [FootnoteType.FOOTNOTE](./#FOOTNOTE)

