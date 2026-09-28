---
title: FootnoteOptions.start_number property
linktitle: start_number property
articleTitle: start_number property
second_title: Aspose.Words for Python
description: "FootnoteOptions.start_number property. Specifies the starting number or character for the first automatically numbered footnotes."
type: docs
weight: 50
url: /zh/python-net/aspose.words.notes/footnoteoptions/start_number/
---

## FootnoteOptions.start_number property

Specifies the starting number or character for the first automatically numbered footnotes.


```python
@property
def start_number(self) -> int:
    ...

@start_number.setter
def start_number(self, value: int):
    ...

```

### Remarks

This property has effect only when [FootnoteOptions.restart_rule](../restart_rule/) is set to
[FootnoteNumberingRule.CONTINUOUS](../../footnotenumberingrule/#CONTINUOUS).




### Examples

Shows how to set a number at which the document begins the footnote/endnote count.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 脚注和尾注是一种将参考或旁注附加到文本的方法
# 它不会干扰正文文本的流畅性。
# 插入脚注/尾注会添加一个小的上标引用符号
# 在我们插入脚注/尾注的正文文本中。
# 每个脚注/尾注还会创建一个条目，该条目由符号组成
# 该符号与正文中的参考符号相匹配。
# 我们传递给文档生成器的 \"InsertEndnote\" 方法的参考文本。
# 默认情况下，脚注条目会显示在包含它们的每页底部
# 它们的引用符号，而尾注则显示在文档末尾。
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.')
builder.insert_paragraph()
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.')
# 默认情况下，每个脚注和尾注的引用符号是它们的索引
# 在文档的所有脚注/尾注中。每个文档维护独立的计数
# 用于脚注和尾注，二者均从 1 开始。
self.assertEqual(1, doc.footnote_options.start_number)
self.assertEqual(1, doc.endnote_options.start_number)
# 我们可以使用 "StartNumber" 属性让文档
# 从不同的数字开始脚注或尾注计数。
doc.endnote_options.number_style = aw.NumberStyle.ARABIC
doc.endnote_options.start_number = 50
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.StartNumber.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

