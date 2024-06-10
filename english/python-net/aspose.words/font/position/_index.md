---
title: Font.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Python
description: "Font.position property. Gets or sets the position of text (in points) relative to the base line"
type: docs
weight: 300
url: /python-net/aspose.words/font/position/
---

## Font.position property

Gets or sets the position of text (in points) relative to the base line.
A positive number raises the text, and a negative number lowers it.


```python
@property
def position(self) -> float:
    ...

@position.setter
def position(self, value: float):
    ...

```

### Examples

Shows how to format text to offset its position.

```python
doc = aw.Document()
para = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
# Raise this run of text 5 points above the baseline.
run = aw.Run(doc=doc, text='Raised text. ')
run.font.position = 5
para.append_child(run)
# Lower this run of text 10 points below the baseline.
run = aw.Run(doc=doc, text='Lowered text. ')
run.font.position = -10
para.append_child(run)
# Add a run of normal text.
run = aw.Run(doc=doc, text='Text in its default position. ')
para.append_child(run)
# Add a run of text that appears as subscript.
run = aw.Run(doc=doc, text='Subscript. ')
run.font.subscript = True
para.append_child(run)
# Add a run of text that appears as superscript.
run = aw.Run(doc=doc, text='Superscript.')
run.font.superscript = True
para.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Font.PositionSubscript.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

