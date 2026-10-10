---
title: EndnoteOptions.restart_rule property
linktitle: restart_rule property
articleTitle: restart_rule property
second_title: Aspose.Words for Python
description: "EndnoteOptions.restart_rule property. Determines when automatic numbering restarts."
type: docs
weight: 30
url: /zh/python-net/aspose.words.notes/endnoteoptions/restart_rule/
---

## EndnoteOptions.restart_rule property

Determines when automatic numbering restarts.


```python
@property
def restart_rule(self) -> aspose.words.notes.FootnoteNumberingRule:
    ...

@restart_rule.setter
def restart_rule(self, value: aspose.words.notes.FootnoteNumberingRule):
    ...

```

### Remarks

Not all values are applicable to endnotes.
To ascertain which values are applicable see [FootnoteNumberingRule](../../footnotenumberingrule/).




### Examples

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

### See Also

* module [aspose.words.notes](../../)
* class [EndnoteOptions](../)

