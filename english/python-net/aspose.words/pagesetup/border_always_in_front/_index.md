---
title: PageSetup.border_always_in_front property
linktitle: border_always_in_front property
articleTitle: border_always_in_front property
second_title: Aspose.Words for Python
description: "PageSetup.border_always_in_front property. Specifies where the page border is positioned relative to intersecting texts and objects."
type: docs
weight: 20
url: /python-net/aspose.words/pagesetup/border_always_in_front/
---

## PageSetup.border_always_in_front property

Specifies where the page border is positioned relative to intersecting texts and objects.


```python
@property
def border_always_in_front(self) -> bool:
    ...

@border_always_in_front.setter
def border_always_in_front(self, value: bool):
    ...

```

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
* class [PageSetup](../)

