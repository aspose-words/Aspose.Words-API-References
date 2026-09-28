---
title: Font.style_identifier property
linktitle: style_identifier property
articleTitle: style_identifier property
second_title: Aspose.Words for Python
description: "Font.style_identifier property. Gets or sets the locale independent style identifier of the character style applied to this formatting."
type: docs
weight: 420
url: /de/python-net/aspose.words/font/style_identifier/
---

## Font.style_identifier property

Gets or sets the locale independent style identifier of the character style applied to this formatting.


```python
@property
def style_identifier(self) -> aspose.words.StyleIdentifier:
    ...

@style_identifier.setter
def style_identifier(self, value: aspose.words.StyleIdentifier):
    ...

```

### Examples

Shows how to change the style of existing text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Unten sind zwei Möglichkeiten, Stile zu referenzieren.
# 1 -  Verwendung des Stilnamens:
builder.font.style_name = 'Emphasis'
builder.writeln('Text originally in "Emphasis" style')
# 2 -  Verwendung eines integrierten Stilidentifikators:
builder.font.style_identifier = aw.StyleIdentifier.INTENSE_EMPHASIS
builder.writeln('Text originally in "Intense Emphasis" style')
# Konvertieren Sie alle Verwendungen eines Stils in einen anderen,
# unter Verwendung der oben genannten Methoden, um alte und neue Stile zu referenzieren.
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

