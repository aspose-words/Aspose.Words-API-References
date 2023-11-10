---
title: PageSetup.left_margin property
linktitle: left_margin property
articleTitle: left_margin property
second_title: Aspose.Words for Python
description: "PageSetup.left_margin property. Returns or sets the distance (in points) between the left edge of the page and the left boundary of the body text."
type: docs
weight: 200
url: /python-net/aspose.words/pagesetup/left_margin/
---

## PageSetup.left_margin property

Returns or sets the distance (in points) between the left edge of the page and the left boundary of the body text.


```python
@property
def left_margin(self) -> float:
    ...

@left_margin.setter
def left_margin(self, value: float):
    ...

```

### Examples

Shows how to adjust paper size, orientation, margins, along with other settings for a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.page_setup.paper_size = aw.PaperSize.LEGAL
builder.page_setup.orientation = aw.Orientation.LANDSCAPE
builder.page_setup.top_margin = aw.ConvertUtil.inch_to_point(1.0)
builder.page_setup.bottom_margin = aw.ConvertUtil.inch_to_point(1.0)
builder.page_setup.left_margin = aw.ConvertUtil.inch_to_point(1.5)
builder.page_setup.right_margin = aw.ConvertUtil.inch_to_point(1.5)
builder.page_setup.header_distance = aw.ConvertUtil.inch_to_point(0.2)
builder.page_setup.footer_distance = aw.ConvertUtil.inch_to_point(0.2)

builder.writeln("Hello world!")

doc.save(ARTIFACTS_DIR + "PageSetup.page_margins.docx")
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

