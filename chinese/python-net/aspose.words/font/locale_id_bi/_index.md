---
title: Font.locale_id_bi property
linktitle: locale_id_bi property
articleTitle: locale_id_bi property
second_title: Aspose.Words for Python
description: "Font.locale_id_bi property. Gets or sets the locale identifier (language) of the formatted right-to-left characters."
type: docs
weight: 210
url: /zh/python-net/aspose.words/font/locale_id_bi/
---

## Font.locale_id_bi property

Gets or sets the locale identifier (language) of the formatted right-to-left characters.


```python
@property
def locale_id_bi(self) -> int:
    ...

@locale_id_bi.setter
def locale_id_bi(self, value: int):
    ...

```

### Remarks

For the list of locale identifiers see https://msdn.microsoft.com/en-us/library/cc233965.aspx


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

