---
title: Font.kerning property
linktitle: kerning property
articleTitle: kerning property
second_title: Aspose.Words for Python
description: "Font.kerning property. Gets or sets the font size at which kerning starts."
type: docs
weight: 180
url: /zh/python-net/aspose.words/font/kerning/
---

## Font.kerning property

Gets or sets the font size at which kerning starts.


```python
@property
def kerning(self) -> float:
    ...

@kerning.setter
def kerning(self, value: float):
    ...

```

### Examples

Shows how to specify the font size at which kerning begins to take effect.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arial Black'
# 设置生成器的字体大小，以及启动字距调整的最小尺寸。
# 字体大小低于字距阈值，因此下面的 run 将不会进行字距调整。
builder.font.size = 18
builder.font.kerning = 24
builder.writeln('TALLY. (Kerning not applied)')
# 设置字距阈值，使生成器当前的字体大小高于该阈值。
# 从此以后我们添加的任何文本都将应用字距调整。字符之间的间距
# 将被调整，通常会使文本 run 看起来更具美感。
builder.font.kerning = 12
builder.writeln('TALLY. (Kerning applied)')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Kerning.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

