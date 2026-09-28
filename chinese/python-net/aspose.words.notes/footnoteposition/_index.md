---
title: FootnotePosition enumeration
linktitle: FootnotePosition enumeration
articleTitle: FootnotePosition enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnotePosition enumeration. Defines the footnote position."
type: docs
weight: 60
url: /zh/python-net/aspose.words.notes/footnoteposition/
---

## FootnotePosition enumeration

Defines the footnote position.


### Members

| Name | Description |
| --- | --- |
| BOTTOM_OF_PAGE | Footnotes are output at the bottom of each page. |
| BENEATH_TEXT | Footnotes are output beneath text on each page. |

### Examples

Shows how to select a different place where the document collects and displays its footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 脚注是一种将参考或旁注附加到文本的方法
# 它不会干扰正文文本的流畅性。
# 插入脚注会添加一个小的上标引用符号
# 在我们插入脚注的正文文本中。
# 每个脚注还会在页面底部创建一个条目，由符号组成
# 该符号与正文中的参考符号相匹配。
# 我们传递给文档生成器的 "InsertFootnote" 方法的引用文本。
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote contents.')
# 我们可以使用 "Position" 属性来确定文档将把所有脚注放置在哪里。
# 如果我们将 "Position" 属性的值设为 "FootnotePosition.BottomOfPage"，
# 每个脚注将在包含其引用标记的页面底部显示。这是默认值。
# 如果我们将 "Position" 属性的值设为 "FootnotePosition.BeneathText"，
# 每个脚注将在包含其引用标记的页面文本末尾显示。
doc.footnote_options.position = footnote_position
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.PositionFootnote.docx')
```

### See Also

* module [aspose.words.notes](../)
* class [FootnoteOptions](../footnoteoptions/)

