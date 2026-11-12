---
title: Font.style property
linktitle: style property
articleTitle: style property
second_title: Aspose.Words for Python
description: "Font.style property. Gets or sets the character style applied to this formatting."
type: docs
weight: 410
url: /tr/python-net/aspose.words/font/style/
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
# Özel bir stil ekleyin ve bunu bir belge oluşturucu kullanarak oluşturulan metne uygulayın.
style = doc.styles.add(aw.StyleType.CHARACTER, 'MyStyle')
style.font.color = aspose.pydrawing.Color.red
style.font.name = 'Courier New'
builder.font.style_name = 'MyStyle'
builder.write('This text is in a custom style.')
# Her koşulu yineleyin ve her özel stile çift alt çizgi ekleyin.
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

