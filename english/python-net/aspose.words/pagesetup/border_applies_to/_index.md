---
title: PageSetup.border_applies_to property
linktitle: border_applies_to property
articleTitle: border_applies_to property
second_title: Aspose.Words for Python
description: "PageSetup.border_applies_to property. Specifies which pages the page border is printed on."
type: docs
weight: 30
url: /python-net/aspose.words/pagesetup/border_applies_to/
---

## PageSetup.border_applies_to property

Specifies which pages the page border is printed on.


```python
@property
def border_applies_to(self) -> aspose.words.PageBorderAppliesTo:
    ...

@border_applies_to.setter
def border_applies_to(self, value: aspose.words.PageBorderAppliesTo):
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

