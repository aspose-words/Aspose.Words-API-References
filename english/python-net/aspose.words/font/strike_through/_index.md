---
title: Font.strike_through property
linktitle: strike_through property
articleTitle: strike_through property
second_title: Aspose.Words for Python
description: "Font.strike_through property. True if the font is formatted as strikethrough text."
type: docs
weight: 400
url: /python-net/aspose.words/font/strike_through/
---

## Font.strike_through property

True if the font is formatted as strikethrough text.


```python
@property
def strike_through(self) -> bool:
    ...

@strike_through.setter
def strike_through(self, value: bool):
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

