---
title: Font.highlight_color property
linktitle: highlight_color property
articleTitle: highlight_color property
second_title: Aspose.Words for Python
description: "Font.highlight_color property. Gets or sets the highlight (marker) color."
type: docs
weight: 150
url: /python-net/aspose.words/font/highlight_color/
---

## Font.highlight_color property

Gets or sets the highlight (marker) color.


```python
@property
def highlight_color(self) -> aspose.pydrawing.Color:
    ...

@highlight_color.setter
def highlight_color(self, value: aspose.pydrawing.Color):
    ...

```

### Examples

Shows how to format a run of text using its font property.

```python
doc = aw.Document()
run = aw.Run(doc=doc, text='Hello world!')
font = run.font
font.name = 'Courier New'
font.size = 36
font.highlight_color = aspose.pydrawing.Color.yellow
doc.first_section.body.first_paragraph.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Font.CreateFormattedRun.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

