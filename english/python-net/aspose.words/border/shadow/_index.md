---
title: Border.shadow property
linktitle: shadow property
articleTitle: shadow property
second_title: Aspose.Words for Python
description: "Border.shadow property. Gets or sets a value indicating whether the border has a shadow."
type: docs
weight: 60
url: /python-net/aspose.words/border/shadow/
---

## Border.shadow property

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

In Microsoft Word, for a border to have a shadow, the borders on all four sides
(left, top, right and bottom) should be of the same type, width, color and all should have
the Shadow property set to ``True``.




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
* class [Border](../)

