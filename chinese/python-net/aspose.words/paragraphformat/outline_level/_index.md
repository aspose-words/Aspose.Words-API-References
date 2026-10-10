---
title: ParagraphFormat.outline_level property
linktitle: outline_level property
articleTitle: outline_level property
second_title: Aspose.Words for Python
description: "ParagraphFormat.outline_level property. Specifies the outline level of the paragraph in the document."
type: docs
weight: 260
url: /zh/python-net/aspose.words/paragraphformat/outline_level/
---

## ParagraphFormat.outline_level property

Specifies the outline level of the paragraph in the document.


```python
@property
def outline_level(self) -> aspose.words.OutlineLevel:
    ...

@outline_level.setter
def outline_level(self, value: aspose.words.OutlineLevel):
    ...

```

### Examples

Shows how to configure paragraph outline levels to create collapsible text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 每个段落都有一个 OutlineLevel，它可以是 1 到 9 的任意数字，或者默认的 \"BodyText\" 值。
# 将属性设置为编号值之一将会在左侧显示一个箭头
# 位于段落开头。
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL1
builder.writeln('Paragraph outline level 1.')
# 级别 1 是最高级别。如果在一个更高级别的段落下面有一个更低级别的段落，
# 折叠更高级别的段落将会折叠更低级别的段落。
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL2
builder.writeln('Paragraph outline level 2.')
# 相同级别的两个段落不会相互折叠，
# 并且箭头不会折叠它们指向的段落。
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL3
builder.writeln('Paragraph outline level 3.')
builder.writeln('Paragraph outline level 3.')
# 默认的 \"BodyText\" 值是最低的，任何级别的段落都可以折叠它。
builder.paragraph_format.outline_level = aw.OutlineLevel.BODY_TEXT
builder.writeln('Paragraph at main text level.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.ParagraphOutlineLevel.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

