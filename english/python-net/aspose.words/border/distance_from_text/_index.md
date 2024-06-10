---
title: Border.distance_from_text property
linktitle: distance_from_text property
articleTitle: distance_from_text property
second_title: Aspose.Words for Python
description: "Border.distance_from_text property. Gets or sets distance of the border from text or from the page edge in points."
type: docs
weight: 20
url: /python-net/aspose.words/border/distance_from_text/
---

## Border.distance_from_text property

Gets or sets distance of the border from text or from the page edge in points.


```python
@property
def distance_from_text(self) -> float:
    ...

@distance_from_text.setter
def distance_from_text(self, value: float):
    ...

```

### Remarks

Has no effect and will be automatically reset to zero for borders of table cells.




### Examples

Shows how to create a wide blue band border at the top of the first page.

```python
doc = aw.Document()
page_setup = doc.sections[0].page_setup
page_setup.border_always_in_front = False
page_setup.border_distance_from = aw.PageBorderDistanceFrom.PAGE_EDGE
page_setup.border_applies_to = aw.PageBorderAppliesTo.FIRST_PAGE
border = page_setup.borders.get_by_border_type(aw.BorderType.TOP)
border.line_style = aw.LineStyle.SINGLE
border.line_width = 30
border.color = aspose.pydrawing.Color.blue
border.distance_from_text = 0
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.PageBorderProperties.docx')
```

### See Also

* module [aspose.words](../../)
* class [Border](../)
* property [PageSetup.border_distance_from](../../pagesetup/border_distance_from/)

