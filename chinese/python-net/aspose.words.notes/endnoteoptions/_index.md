---
title: EndnoteOptions class
linktitle: EndnoteOptions class
articleTitle: EndnoteOptions class
second_title: Aspose.Words for Python
description: "aspose.words.notes.EndnoteOptions class. Represents the endnote numbering options for a document or section"
type: docs
weight: 10
url: /zh/python-net/aspose.words.notes/endnoteoptions/
---

## EndnoteOptions class

Represents the endnote numbering options for a document or section.
To learn more, visit the [Working with Footnote and Endnote](https://docs.aspose.com/words/python-net/working-with-footnote-and-endnote/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [number_style](./number_style/) | Specifies the number format for automatically numbered endnotes. |
| [position](./position/) | Specifies the endnotes position. |
| [restart_rule](./restart_rule/) | Determines when automatic numbering restarts. |
| [start_number](./start_number/) | Specifies the starting number or character for the first automatically numbered endnotes. |

### Examples

Shows how to select a different place where the document collects and displays its endnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 尾注是一种将参考或旁注附加到文本的方法
# 它不会干扰正文文本的流畅性。
# 插入尾注会添加一个小的上标参考符号
# 在我们插入尾注的正文文本位置。
# 每个尾注还会在文档末尾创建一个条目，由符号组成
# 该符号与正文中的参考符号相匹配。
# 我们传递给文档生成器的 \"InsertEndnote\" 方法的参考文本。
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote contents.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('This is the second section.')
# 我们可以使用 \"Position\" 属性来确定文档将把所有尾注放置在哪里。
# 如果我们将 \"Position\" 属性的值设置为 \"EndnotePosition.EndOfDocument\",
# 每个脚注都会出现在文档末尾的集合中。这是默认值。
# 如果我们将 \"Position\" 属性的值设置为 \"EndnotePosition.EndOfSection\",
# 每个脚注将在包含尾注引用标记的章节末尾的集合中显示。
doc.endnote_options.position = endnote_position
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.PositionEndnote.docx')
```

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

Shows how to restart footnote/endnote numbering at certain places in the document.

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
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.')
builder.write('Text 4. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 4.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.')
builder.write('Text 4. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 4.')
# 默认情况下，每个脚注和尾注的引用符号是它们的索引
# 在文档的所有脚注/尾注中。每个文档维护独立的计数
# 适用于脚注和尾注，并且在任何时候都不会重新计数。
self.assertEqual(doc.footnote_options.restart_rule, aw.notes.FootnoteNumberingRule.DEFAULT)
self.assertEqual(aw.notes.FootnoteNumberingRule.DEFAULT, aw.notes.FootnoteNumberingRule.CONTINUOUS)
# 我们可以使用 "RestartRule" 属性让文档重新开始
# 脚注/尾注计数在新页面或章节中。
doc.footnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_PAGE
doc.endnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_SECTION
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.NumberingRule.docx')
```

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

* module [aspose.words.notes](../)
* property [Document.endnote_options](../../aspose.words/document/endnote_options/)
* property [PageSetup.endnote_options](../../aspose.words/pagesetup/endnote_options/)

