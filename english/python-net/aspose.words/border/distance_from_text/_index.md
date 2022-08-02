---
title: distance_from_text property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets distance of the border from text or from the page edge in points."
type: docs
weight: 20
url: /python-net/aspose.words/border/distance_from_text/
---

## Border.distance_from_text property

Gets or sets distance of the border from text or from the page edge in points.

Has no effect and will be automatically reset to zero for borders of table cells.




### Examples

Shows how to create a wide blue band border at the top of the first page.

```python
doc = aw.Document()

page_setup = doc.sections[0].page_setup
page_setup.border_always_in_front = False
page_setup.border_distance_from = aw.PageBorderDistanceFrom.PAGE_EDGE
page_setup.border_applies_to = aw.PageBorderAppliesTo.FIRST_PAGE

border = page_setup.borders.top
border.line_style = aw.LineStyle.SINGLE
border.line_width = 30
border.color = drawing.Color.blue
border.distance_from_text = 0

doc.save(ARTIFACTS_DIR + "PageSetup.page_border_properties.docx")
```

### See Also

* module [aspose.words](../../)
* class [Border](../)
* property [PageSetup.border_distance_from](../../pagesetup/border_distance_from/)

