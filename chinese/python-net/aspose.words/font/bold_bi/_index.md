---
title: Font.bold_bi property
linktitle: bold_bi property
articleTitle: bold_bi property
second_title: Aspose.Words for Python
description: "Font.bold_bi property. True if the right-to-left text is formatted as bold."
type: docs
weight: 50
url: /zh/python-net/aspose.words/font/bold_bi/
---

## Font.bold_bi property

True if the right-to-left text is formatted as bold.


```python
@property
def bold_bi(self) -> bool:
    ...

@bold_bi.setter
def bold_bi(self, value: bool):
    ...

```

### Examples

Shows how to define separate sets of font settings for right-to-left, and right-to-left text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# 为从左到右的文本定义一组字体设置。
builder.font.name = 'Courier New'
builder.font.size = 16
builder.font.italic = False
builder.font.bold = False
builder.font.locale_id = 1033  # en-US
# 为从右到左的文本定义另一组字体设置。
builder.font.name_bi = 'Andalus'
builder.font.size_bi = 24
builder.font.italic_bi = True
builder.font.bold_bi = True
builder.font.locale_id_bi = 4096  # ar-AR
# 我们可以使用 "bidi" 标志来指示即将添加的文本是否
# 使用文档生成器时为从右到左。当我们将此标志设为 True 添加文本时，
# 它将使用从右到左的字体设置进行格式化。
builder.font.bidi = True
builder.write('مرحبًا')
# 将标志设置为 "False"，然后添加从左到右的文本。
# 文档生成器将使用从左到右的字体设置对这些进行格式化。
builder.font.bidi = False
builder.write(' Hello world!')
doc.save(ARTIFACTS_DIR + 'Font.bidi.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

