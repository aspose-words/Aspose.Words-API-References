---
title: position property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the position of text (in points) relative to the base line"
type: docs
weight: 300
url: /python-net/aspose.words/font/position/
---

## Font.position property

Gets or sets the position of text (in points) relative to the base line.
A positive number raises the text, and a negative number lowers it.


### Examples

Shows how to format text to offset its position.

```python
doc = aw.Document()
para = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()

# Raise this run of text 5 points above the baseline.
run = aw.Run(doc, "Raised text. ")
run.font.position = 5
para.append_child(run)

# Lower this run of text 10 points below the baseline.
run = aw.Run(doc, "Lowered text. ")
run.font.position = -10
para.append_child(run)

# Add a run of normal text.
run = aw.Run(doc, "Text in its default position. ")
para.append_child(run)

# Add a run of text that appears as subscript.
run = aw.Run(doc, "Subscript. ")
run.font.subscript = True
para.append_child(run)

# Add a run of text that appears as superscript.
run = aw.Run(doc, "Superscript.")
run.font.superscript = True
para.append_child(run)

doc.save(ARTIFACTS_DIR + "Font.position_subscript.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

