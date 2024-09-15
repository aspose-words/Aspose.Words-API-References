---
title: PageSetup.header_distance property
linktitle: header_distance property
articleTitle: header_distance property
second_title: Aspose.Words for Python
description: "PageSetup.header_distance property. Returns or sets the distance (in points) between the header and the top of the page."
type: docs
weight: 170
url: /python-net/aspose.words/pagesetup/header_distance/
---

## PageSetup.header_distance property

Returns or sets the distance (in points) between the header and the top of the page.


```python
@property
def header_distance(self) -> float:
    ...

@header_distance.setter
def header_distance(self, value: float):
    ...

```

### Examples

Shows how to adjust paper size, orientation, margins, along with other settings for a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.page_setup.paper_size = aw.PaperSize.LEGAL
builder.page_setup.orientation = aw.Orientation.LANDSCAPE
builder.page_setup.top_margin = aw.ConvertUtil.inch_to_point(1)
builder.page_setup.bottom_margin = aw.ConvertUtil.inch_to_point(1)
builder.page_setup.left_margin = aw.ConvertUtil.inch_to_point(1.5)
builder.page_setup.right_margin = aw.ConvertUtil.inch_to_point(1.5)
builder.page_setup.header_distance = aw.ConvertUtil.inch_to_point(0.2)
builder.page_setup.footer_distance = aw.ConvertUtil.inch_to_point(0.2)
builder.writeln('Hello world!')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.PageMargins.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

