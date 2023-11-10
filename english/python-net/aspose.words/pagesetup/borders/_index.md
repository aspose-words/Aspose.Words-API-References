---
title: PageSetup.borders property
linktitle: borders property
articleTitle: borders property
second_title: Aspose.Words for Python
description: "PageSetup.borders property. Gets a collection of the page borders."
type: docs
weight: 70
url: /python-net/aspose.words/pagesetup/borders/
---

## PageSetup.borders property

Gets a collection of the page borders.


```python
@property
def borders(self) -> aspose.words.BorderCollection:
    ...

```

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
* class [PageSetup](../)

