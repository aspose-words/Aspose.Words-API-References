---
title: PageBorderAppliesTo enumeration
linktitle: PageBorderAppliesTo enumeration
articleTitle: PageBorderAppliesTo enumeration
second_title: Aspose.Words for Python
description: "aspose.words.PageBorderAppliesTo enumeration. Specifies which pages the page border is printed on."
type: docs
weight: 840
url: /python-net/aspose.words/pageborderappliesto/
---

## PageBorderAppliesTo enumeration

Specifies which pages the page border is printed on.


### Members

| Name | Description |
| --- | --- |
| ALL_PAGES | Page border is shown on all pages of the section. |
| FIRST_PAGE | Page border is shown on the first page of the section only. |
| OTHER_PAGES | Page border is shown on all pages except the first page of the section. |

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
* property [PageSetup.border_applies_to](../pagesetup/border_applies_to/)

