---
title: Font.double_strike_through property
linktitle: double_strike_through property
articleTitle: double_strike_through property
second_title: Aspose.Words for Python
description: "Font.double_strike_through property. True if the font is formatted as double strikethrough text."
type: docs
weight: 90
url: /python-net/aspose.words/font/double_strike_through/
---

## Font.double_strike_through property

True if the font is formatted as double strikethrough text.


```python
@property
def double_strike_through(self) -> bool:
    ...

@double_strike_through.setter
def double_strike_through(self, value: bool):
    ...

```

### Examples

Shows how to add a line strikethrough to text.

```python
doc = aw.Document()
para = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
run = aw.Run(doc=doc, text='Text with a single-line strikethrough.')
run.font.strike_through = True
para.append_child(run)
para = para.parent_node.append_child(aw.Paragraph(doc)).as_paragraph()
run = aw.Run(doc=doc, text='Text with a double-line strikethrough.')
run.font.double_strike_through = True
para.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Font.StrikeThrough.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

