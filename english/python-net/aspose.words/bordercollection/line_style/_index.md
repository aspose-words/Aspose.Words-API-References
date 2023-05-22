---
title: BorderCollection.line_style property
linktitle: line_style property
articleTitle: line_style property
second_title: Aspose.Words for Python
description: "BorderCollection.line_style property. Gets or sets the border style."
type: docs
weight: 80
url: /python-net/aspose.words/bordercollection/line_style/
---

## BorderCollection.line_style property

Gets or sets the border style.

Returns the style of the first border in the collection.

Sets the style of all borders in the collection excluding diagonal borders.




### Examples

Shows how to create green wavy page border with a shadow.

```python
doc = aw.Document()
page_setup = doc.sections[0].page_setup

page_setup.borders.line_style = aw.LineStyle.DOUBLE_WAVE
page_setup.borders.line_width = 2
page_setup.borders.color = drawing.Color.green
page_setup.borders.distance_from_text = 24
page_setup.borders.shadow = True

doc.save(ARTIFACTS_DIR + "PageSetup.page_borders.docx")
```

### See Also

* module [aspose.words](../../)
* class [BorderCollection](../)

