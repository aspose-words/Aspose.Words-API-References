---
title: BorderCollection.distance_from_text property
linktitle: distance_from_text property
articleTitle: distance_from_text property
second_title: Aspose.Words for Python
description: "BorderCollection.distance_from_text property. Gets or sets distance of the border from text in points."
type: docs
weight: 50
url: /python-net/aspose.words/bordercollection/distance_from_text/
---

## BorderCollection.distance_from_text property

Gets or sets distance of the border from text in points.


```python
@property
def distance_from_text(self) -> float:
    ...

@distance_from_text.setter
def distance_from_text(self, value: float):
    ...

```

### Remarks

Gets the distance from text for the first border.

Sets the distance from text for all borders in the collection excluding diagonal borders.

Has no effect and will be automatically reset to zero for borders of table cells.




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

