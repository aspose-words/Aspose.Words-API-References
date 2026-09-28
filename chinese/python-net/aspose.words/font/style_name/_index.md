---
title: Font.style_name property
linktitle: style_name property
articleTitle: style_name property
second_title: Aspose.Words for Python
description: "Font.style_name property. Gets or sets the name of the character style applied to this formatting."
type: docs
weight: 430
url: /zh/python-net/aspose.words/font/style_name/
---

## Font.style_name property

Gets or sets the name of the character style applied to this formatting.


```python
@property
def style_name(self) -> str:
    ...

@style_name.setter
def style_name(self, value: str):
    ...

```

### Examples

Shows how to change the style of existing text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 下面是引用样式的两种方式。
# 1 -  使用样式名称：
builder.font.style_name = 'Emphasis'
builder.writeln('Text originally in "Emphasis" style')
# 2 -  使用内置样式标识符：
builder.font.style_identifier = aw.StyleIdentifier.INTENSE_EMPHASIS
builder.writeln('Text originally in "Intense Emphasis" style')
# 将一种样式的所有使用转换为另一种，
# 使用上述方法引用旧样式和新样式。
for run in doc.get_child_nodes(aw.NodeType.RUN, True):
    run = run.as_run()
    if run.font.style_name == 'Emphasis':
        run.font.style_name = 'Strong'
    if run.font.style_identifier == aw.StyleIdentifier.INTENSE_EMPHASIS:
        run.font.style_identifier = aw.StyleIdentifier.STRONG
doc.save(file_name=ARTIFACTS_DIR + 'Font.ChangeStyle.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

