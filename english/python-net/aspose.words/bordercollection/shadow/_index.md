---
title: BorderCollection.shadow property
linktitle: shadow property
articleTitle: shadow property
second_title: Aspose.Words for Python
description: "BorderCollection.shadow property. Gets or sets a value indicating whether the border has a shadow."
type: docs
weight: 110
url: /python-net/aspose.words/bordercollection/shadow/
---

## BorderCollection.shadow property

Gets or sets a value indicating whether the border has a shadow.


```python
@property
def shadow(self) -> bool:
    ...

@shadow.setter
def shadow(self, value: bool):
    ...

```

### Remarks

Gets the value from the first border in the collection.

Sets the value for all borders in the collection excluding diagonal borders.




### Examples

Shows how to create green wavy page border with a shadow.

```python
doc = aw.Document()
page_setup = doc.sections[0].page_setup
page_setup.borders.line_style = aw.LineStyle.DOUBLE_WAVE
page_setup.borders.line_width = 2
page_setup.borders.color = aspose.pydrawing.Color.green
page_setup.borders.distance_from_text = 24
page_setup.borders.shadow = True
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.PageBorders.docx')
```

### See Also

* module [aspose.words](../../)
* class [BorderCollection](../)

