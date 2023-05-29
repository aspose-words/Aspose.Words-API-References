---
title: PageSetup.border_distance_from property
linktitle: border_distance_from property
articleTitle: border_distance_from property
second_title: Aspose.Words for Python
description: "PageSetup.border_distance_from property. Gets or sets a value that indicates whether the specified page border is measured from the edge of the page or from the text it surrounds."
type: docs
weight: 40
url: /python-net/aspose.words/pagesetup/border_distance_from/
---

## PageSetup.border_distance_from property

Gets or sets a value that indicates whether the specified page border is measured from the edge of the page or from the text it surrounds.


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
* class [PageSetup](../)

