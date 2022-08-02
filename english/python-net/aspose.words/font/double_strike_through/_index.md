---
title: double_strike_through property
second_title: Aspose.Words for Python via .NET API Reference
description: "True if the font is formatted as double strikethrough text."
type: docs
weight: 90
url: /python-net/aspose.words/font/double_strike_through/
---

## Font.double_strike_through property

True if the font is formatted as double strikethrough text.


### Examples

Shows how to add a line strikethrough to text.

```python
doc = aw.Document()
para = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()

run = aw.Run(doc, "Text with a single-line strikethrough.")
run.font.strike_through = True
para.append_child(run)

para = para.parent_node.append_child(aw.Paragraph(doc)).as_paragraph()

run = aw.Run(doc, "Text with a double-line strikethrough.")
run.font.double_strike_through = True
para.append_child(run)

doc.save(ARTIFACTS_DIR + "Font.strike_through.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

