---
title: Footnote.is_auto property
linktitle: is_auto property
articleTitle: is_auto property
second_title: Aspose.Words for Python
description: "Footnote.is_auto property. Holds a value that specifies whether this is a auto-numbered footnote or  footnote with user defined custom reference mark."
type: docs
weight: 40
url: /zh/python-net/aspose.words.notes/footnote/is_auto/
---

## Footnote.is_auto property

Holds a value that specifies whether this is a auto-numbered footnote or 
footnote with user defined custom reference mark.


```python
@property
def is_auto(self) -> bool:
    ...

@is_auto.setter
def is_auto(self, value: bool):
    ...

```

### Remarks

[Footnote.reference_mark](../reference_mark/) initialized with empty string if [Footnote.is_auto](./) set to ``False``.



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

### See Also

* module [aspose.words.notes](../../)
* class [Footnote](../)

