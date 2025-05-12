---
title: PageRange class
linktitle: PageRange class
articleTitle: PageRange class
second_title: Aspose.Words for Python
description: "aspose.words.saving.PageRange class. Represents a continuous range of pages"
type: docs
weight: 560
url: /python-net/aspose.words.saving/pagerange/
---

## PageRange class

Represents a continuous range of pages.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/python-net/programming-with-documents/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [PageRange(from_address, to)](./__init__/#int_int) | Creates a new page range object. |

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

* module [aspose.words.saving](../)

