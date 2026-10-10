---
title: Font.spacing property
linktitle: spacing property
articleTitle: spacing property
second_title: Aspose.Words for Python
description: "Font.spacing property. Returns or sets the spacing (in points) between characters ."
type: docs
weight: 390
url: /zh/python-net/aspose.words/font/spacing/
---

## Font.spacing property

Returns or sets the spacing (in points) between characters .


```python
@property
def spacing(self) -> float:
    ...

@spacing.setter
def spacing(self, value: float):
    ...

```

### Examples

Shows how to set horizontal scaling and spacing for characters.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 添加文本 run 并将字符宽度增加到 150%。
builder.font.scaling = 150
builder.writeln('Wide characters')
# 添加文本 run 并在每个字符之间添加 1pt 的额外水平间距。
builder.font.spacing = 1
builder.writeln('Expanded by 1pt')
# 添加文本 run 并将字符间距缩小 1pt。
builder.font.spacing = -1
builder.writeln('Condensed by 1pt')
doc.save(file_name=ARTIFACTS_DIR + 'Font.ScalingSpacing.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

