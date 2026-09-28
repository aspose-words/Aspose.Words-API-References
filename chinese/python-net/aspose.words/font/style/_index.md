---
title: Font.style property
linktitle: style property
articleTitle: style property
second_title: Aspose.Words for Python
description: "Font.style property. Gets or sets the character style applied to this formatting."
type: docs
weight: 410
url: /zh/python-net/aspose.words/font/style/
---

## Font.style property

Gets or sets the character style applied to this formatting.


```python
@property
def style(self) -> aspose.words.Style:
    ...

@style.setter
def style(self, value: aspose.words.Style):
    ...

```

### Examples

Applies a double underline to all runs in a document that are formatted with custom character styles.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 插入自定义样式并将其应用于使用文档构建器创建的文本。
style = doc.styles.add(aw.StyleType.CHARACTER, 'MyStyle')
style.font.color = aspose.pydrawing.Color.red
style.font.name = 'Courier New'
builder.font.style_name = 'MyStyle'
builder.write('This text is in a custom style.')
# 遍历每个运行，并为每个自定义样式添加双下划线。
for run in doc.get_child_nodes(aw.NodeType.RUN, True):
    run = run.as_run()
    char_style = run.font.style
    if not char_style.built_in:
        run.font.underline = aw.Underline.DOUBLE
doc.save(file_name=ARTIFACTS_DIR + 'Font.Style.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

