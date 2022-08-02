---
title: highlight_color property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the highlight (marker) color."
type: docs
weight: 150
url: /python-net/aspose.words/font/highlight_color/
---

## Font.highlight_color property

Gets or sets the highlight (marker) color.


### Examples

Shows how to format a run of text using its font property.

```python
doc = aw.Document()
run = aw.Run(doc, "Hello world!")

font = run.font
font.name = "Courier New"
font.size = 36
font.highlight_color = drawing.Color.yellow

doc.first_section.body.first_paragraph.append_child(run)
doc.save(ARTIFACTS_DIR + "Font.create_formatted_run.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

