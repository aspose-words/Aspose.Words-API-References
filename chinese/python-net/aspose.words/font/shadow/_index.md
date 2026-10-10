---
title: Font.shadow property
linktitle: shadow property
articleTitle: shadow property
second_title: Aspose.Words for Python
description: "Font.shadow property. True if the font is formatted as shadowed."
type: docs
weight: 340
url: /zh/python-net/aspose.words/font/shadow/
---

## Font.shadow property

True if the font is formatted as shadowed.


```python
@property
def shadow(self) -> bool:
    ...

@shadow.setter
def shadow(self, value: bool):
    ...

```

### Examples

Shows how to create a run of text formatted with a shadow.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 设置 Shadow 标志以应用偏移阴影效果，
# 使字母看起来像漂浮在页面上方。
builder.font.shadow = True
builder.font.size = 36
builder.writeln('This text has a shadow.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Shadow.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

