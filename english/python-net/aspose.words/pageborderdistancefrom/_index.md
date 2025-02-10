---
title: PageBorderDistanceFrom enumeration
linktitle: PageBorderDistanceFrom enumeration
articleTitle: PageBorderDistanceFrom enumeration
second_title: Aspose.Words for Python
description: "aspose.words.PageBorderDistanceFrom enumeration. Specifies the positioning of the page border relative to the page margin."
type: docs
weight: 850
url: /python-net/aspose.words/pageborderdistancefrom/
---

## PageBorderDistanceFrom enumeration

Specifies the positioning of the page border relative to the page margin.


### Members

| Name | Description |
| --- | --- |
| TEXT | Border position is measured from the page margin. |
| PAGE_EDGE | Border position is measured from the page edge. |

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

* module [aspose.words](../)
* class [PageSetup](../pagesetup/)
* property [PageSetup.border_distance_from](../pagesetup/border_distance_from/)

