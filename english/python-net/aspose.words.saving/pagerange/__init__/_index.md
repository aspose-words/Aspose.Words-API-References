---
title: PageRange constructor
second_title: Aspose.Words for Python via .NET API Reference
description: "Creates a new page range object."
type: docs
weight: 10
url: /python-net/aspose.words.saving/pagerange/__init__/
---

## PageRange(from_address, to) {#int_int}

Creates a new page range object.


```python
def __init__(self, from_address: int, to: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| from_address | int |  |
| to | int |  |

System.Int32.MaxValue means the last page in the document.



### Examples

Shows how to extract pages based on exact page ranges.

```python
doc = aw.Document(MY_DIR + "Images.docx")

image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
ranges = [
    aw.saving.PageRange(1, 1),
    aw.saving.PageRange(2, 3),
    aw.saving.PageRange(1, 3),
    aw.saving.PageRange(2, 4),
    aw.saving.PageRange(1, 1)
    ]
page_set = aw.saving.PageSet(ranges=ranges)

image_options.page_set = page_set
doc.save(ARTIFACTS_DIR + "ImageSaveOptions.export_various_page_ranges.tiff", image_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PageRange](../)

