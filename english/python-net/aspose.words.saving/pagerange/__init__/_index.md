---
title: PageRange constructor
linktitle: PageRange constructor
articleTitle: PageRange constructor
second_title: Aspose.Words for Python
description: "PageRange constructor. Creates a new page range object."
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
| from_address | int | The starting page zero-based index. |
| to | int | The ending page zero-based index.  If it exceeds the index of the last page in the document,  it is truncated to fit in the document on rendering. |

### Remarks

int.MaxValue C# constant means the last page in the document.



### Examples

Shows how to extract pages based on exact page ranges.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
page_set = aw.saving.PageSet(ranges=[aw.saving.PageRange(1, 1), aw.saving.PageRange(2, 3), aw.saving.PageRange(1, 3), aw.saving.PageRange(2, 4), aw.saving.PageRange(1, 1)])
image_options.page_set = page_set
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.ExportVariousPageRanges.tiff', save_options=image_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PageRange](../)

