---
title: Font.name_ascii property
linktitle: name_ascii property
articleTitle: name_ascii property
second_title: Aspose.Words for Python
description: "Font.name_ascii property. Returns or sets the font used for Latin text (characters with character codes from 0 (zero) through 127)."
type: docs
weight: 240
url: /zh/python-net/aspose.words/font/name_ascii/
---

## Font.name_ascii property

Returns or sets the font used for Latin text (characters with character codes from 0 (zero) through 127).


```python
@property
def name_ascii(self) -> str:
    ...

@name_ascii.setter
def name_ascii(self, value: str):
    ...

```

### Examples

Shows how Microsoft Word can combine two different fonts in one run.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 假设我们在使用此字体配置时，通过生成器插入的一个 run
# 包含在 ASCII 字符范围内的字符。在这种情况下，
# 它将使用此字体显示这些字符。
builder.font.name_ascii = 'Calibri'
# 如果未指定其他字体，构建器也会将此字体应用于它插入的所有字符。
self.assertEqual('Calibri', builder.font.name)
# 指定一种字体用于所有超出 ASCII 范围的字符。
# 理想情况下，此字体应为每个所需的非 ASCII 字符码提供字形。
builder.font.name_other = 'Courier New'
# 插入一个运行，其中一个单词由 ASCII 字符组成，另一个单词包含所有超出该范围的字符。
# 每个字符将根据情况使用其中一种字体进行显示。
builder.writeln('Hello, Привет')
doc.save(file_name=ARTIFACTS_DIR + 'Font.NameAscii.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)
* property [Font.name](../name/)

