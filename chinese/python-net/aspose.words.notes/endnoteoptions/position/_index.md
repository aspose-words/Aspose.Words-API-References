---
title: EndnoteOptions.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Python
description: "EndnoteOptions.position property. Specifies the endnotes position."
type: docs
weight: 20
url: /zh/python-net/aspose.words.notes/endnoteoptions/position/
---

## EndnoteOptions.position property

Specifies the endnotes position.


```python
@property
def position(self) -> aspose.words.notes.EndnotePosition:
    ...

@position.setter
def position(self, value: aspose.words.notes.EndnotePosition):
    ...

```

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

### See Also

* module [aspose.words.notes](../../)
* class [EndnoteOptions](../)

