---
title: Paragraph.break_is_style_separator property
linktitle: break_is_style_separator property
articleTitle: break_is_style_separator property
second_title: Aspose.Words for Python
description: "Paragraph.break_is_style_separator property. True if this paragraph break is a Style Separator"
type: docs
weight: 20
url: /zh/python-net/aspose.words/paragraph/break_is_style_separator/
---

## Paragraph.break_is_style_separator property

True if this paragraph break is a Style Separator. A style separator allows one
paragraph to consist of parts that have different paragraph styles.


```python
@property
def break_is_style_separator(self) -> bool:
    ...

```

### Examples

Shows how to write text to the same line as a TOC heading and have it not show up in the TOC.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_table_of_contents('\\o \\h \\z \\u')
builder.insert_break(aw.BreakType.PAGE_BREAK)
# 插入一个段落，并使用 TOC 将其识别为条目的样式。
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
# 这两个字符串位于同一段落中，因此将在同一 TOC 条目中显示。
builder.write('Heading 1. ')
builder.write('Will appear in the TOC. ')
# 如果我们插入样式分隔符，就可以在同一段落中写入更多文本
# 并使用不同的样式且不会显示在目录中。
# 如果我们在分隔符后使用标题类型样式，就可以从文档中的一行文本生成多个目录条目。
builder.insert_style_separator()
builder.paragraph_format.style_identifier = aw.StyleIdentifier.QUOTE
builder.write("Won't appear in the TOC. ")
self.assertTrue(doc.first_section.body.first_paragraph.break_is_style_separator)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Paragraph.BreakIsStyleSeparator.docx')
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

