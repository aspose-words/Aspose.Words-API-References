---
title: Font.small_caps property
linktitle: small_caps property
articleTitle: small_caps property
second_title: Aspose.Words for Python
description: "Font.small_caps property. True if the font is formatted as small capital letters."
type: docs
weight: 370
url: /de/python-net/aspose.words/font/small_caps/
---

## Font.small_caps property

True if the font is formatted as small capital letters.


```python
@property
def small_caps(self) -> bool:
    ...

@small_caps.setter
def small_caps(self, value: bool):
    ...

```

### Examples

Shows how to format a run to display its contents in capitals.

```python
doc = aw.Document()
para = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
# Es gibt zwei Möglichkeiten, einen Lauf dazu zu bringen, seinen Kleinbuchstabentext in Großbuchstaben anzuzeigen, ohne den Inhalt zu ändern.
# 1 -  Setzen Sie das AllCaps‑Flag, um alle Zeichen in regulären Großbuchstaben anzuzeigen:
run = aw.Run(doc=doc, text='all capitals')
run.font.all_caps = True
para.append_child(run)
para = para.parent_node.append_child(aw.Paragraph(doc)).as_paragraph()
# 2 -  Setzen Sie das SmallCaps‑Flag, um alle Zeichen in Kapitälchen anzuzeigen:
# Wenn ein Zeichen klein geschrieben ist, erscheint es in seiner Großbuchstabenform
# aber hat dieselbe Höhe wie das Kleinbuchstaben (die x‑Höhe der Schrift).
# Zeichen, die ursprünglich in Großbuchstaben waren, sehen gleich aus.
run = aw.Run(doc=doc, text='Small Capitals')
run.font.small_caps = True
para.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Font.Caps.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

