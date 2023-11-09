---
title: BorderCollection.color property
linktitle: color property
articleTitle: color property
second_title: Aspose.Words for Python
description: "BorderCollection.color property. Gets or sets the border color."
type: docs
weight: 30
url: /python-net/aspose.words/bordercollection/color/
---

## BorderCollection.color property

Gets or sets the border color.


```python
@property
def color(self) -> aspose.pydrawing.Color:
    ...

@color.setter
def color(self, value: aspose.pydrawing.Color):
    ...

```

### Remarks

Returns the color of the first border in the collection.

Sets the color of all borders in the collection excluding diagonal borders.




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

