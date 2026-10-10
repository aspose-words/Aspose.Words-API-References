---
title: Footnote.reference_mark property
linktitle: reference_mark property
articleTitle: reference_mark property
second_title: Aspose.Words for Python
description: "Footnote.reference_mark property. Gets/sets custom reference mark to be used for this footnote"
type: docs
weight: 60
url: /zh/python-net/aspose.words.notes/footnote/reference_mark/
---

## Footnote.reference_mark property

Gets/sets custom reference mark to be used for this footnote.
Default value is **empty string** (), meaning auto-numbered footnotes are used.



```python
@property
def reference_mark(self) -> str:
    ...

@reference_mark.setter
def reference_mark(self, value: str):
    ...

```

### Remarks

If this property is set to **empty string** () or ``None``, then [Footnote.is_auto](../is_auto/) property will automatically be set to ``True``, 
if set to anything else then [Footnote.is_auto](../is_auto/) will be set to ``False``.


RTF-format can only store 1 symbol as custom reference mark, so upon export only the first symbol will be written others will be discard.




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

