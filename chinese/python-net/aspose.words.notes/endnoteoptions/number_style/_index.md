---
title: EndnoteOptions.number_style property
linktitle: number_style property
articleTitle: number_style property
second_title: Aspose.Words for Python
description: "EndnoteOptions.number_style property. Specifies the number format for automatically numbered endnotes."
type: docs
weight: 10
url: /zh/python-net/aspose.words.notes/endnoteoptions/number_style/
---

## EndnoteOptions.number_style property

Specifies the number format for automatically numbered endnotes.


```python
@property
def number_style(self) -> aspose.words.NumberStyle:
    ...

@number_style.setter
def number_style(self, value: aspose.words.NumberStyle):
    ...

```

### Remarks

Not all number styles are applicable for this property. For the list of applicable
number styles see the Insert Footnote or Endnote dialog box in Microsoft Word. If you select
a number style that is not applicable, Microsoft Word will revert to a default value.




### Examples

Shows how to change the number style of footnote/endnote reference marks.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 脚注和尾注是一种将参考或旁注附加到文本的方法
# 它不会干扰正文文本的流畅性。
# 插入脚注/尾注会添加一个小的上标引用符号
# 在我们插入脚注/尾注的正文文本中。
# 每个脚注/尾注还会创建一个条目，由与引用相匹配的符号组成
# 正文中的符号。我们传递给文档生成器的 "InsertEndnote" 方法的引用文本。
# 默认情况下，脚注条目会显示在包含它们的每页底部
# 它们的引用符号，而尾注则显示在文档末尾。
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.', reference_mark='Custom footnote reference mark')
builder.insert_paragraph()
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.', reference_mark='Custom endnote reference mark')
# 默认情况下，每个脚注和尾注的引用符号是它们的索引
# 在文档的所有脚注/尾注中。每个文档维护独立的计数
# 分别用于脚注和尾注。默认情况下，脚注使用阿拉伯数字显示其编号，
# 而尾注使用小写罗马数字显示其编号。
self.assertEqual(aw.NumberStyle.ARABIC, doc.footnote_options.number_style)
self.assertEqual(aw.NumberStyle.LOWERCASE_ROMAN, doc.endnote_options.number_style)
# 我们可以使用 "NumberStyle" 属性为脚注和尾注应用自定义编号样式。
# 这不会影响具有自定义引用标记的脚注/尾注。
doc.footnote_options.number_style = aw.NumberStyle.UPPERCASE_ROMAN
doc.endnote_options.number_style = aw.NumberStyle.UPPERCASE_LETTER
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.RefMarkNumberStyle.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [EndnoteOptions](../)

