---
title: ParagraphFormat.right_indent property
linktitle: right_indent property
articleTitle: right_indent property
second_title: Aspose.Words for Python
description: "ParagraphFormat.right_indent property. Gets or sets the value (in points) that represents the right indent for paragraph."
type: docs
weight: 280
url: /zh/python-net/aspose.words/paragraphformat/right_indent/
---

## ParagraphFormat.right_indent property

Gets or sets the value (in points) that represents the right indent for paragraph.


```python
@property
def right_indent(self) -> float:
    ...

@right_indent.setter
def right_indent(self, value: float):
    ...

```

### Examples

Shows how to configure paragraph formatting to create off-center text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 居中文档构建器写入的所有文本，并设置缩进。
# 下面的缩进配置将创建一个在页面上不对称排列的文本主体。
# 我们对齐文本的 “center” 将是文本主体的中间，而不是页面的中间。
paragraph_format = builder.paragraph_format
paragraph_format.alignment = aw.ParagraphAlignment.CENTER
paragraph_format.left_indent = 100
paragraph_format.right_indent = 50
paragraph_format.space_after = 25
builder.writeln('This paragraph demonstrates how left and right indentation affects word wrapping.')
builder.writeln("The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.")
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.SetParagraphFormatting.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

