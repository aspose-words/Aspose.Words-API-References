---
title: PageSet constructor
linktitle: PageSet constructor
articleTitle: PageSet constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.PageSet constructor"
type: docs
weight: 10
url: /python-net/aspose.words.saving/pageset/__init__/
---

## PageSet(page) {#int}

Creates an one-page set based on exact page index.


```python
def __init__(self, page: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| page | int |  |

If a page is encountered that is not in the document, an exception will be thrown during rendering.
System.Int32.MaxValue means the last page in the document.



## PageSet(pages) {#intlist}

Creates a page set based on exact page indices.


```python
def __init__(self, pages: List[int]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| pages | List[int] |  |

If a page is encountered that is not in the document, an exception will be thrown during rendering.
System.Int32.MaxValue means the last page in the document.



## PageSet(ranges) {#pagerangelist}

Creates a page set based on ranges.


```python
def __init__(self, ranges: List[aspose.words.saving.PageRange]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| ranges | List[[PageRange](../../pagerange/)] |  |

If a range is encountered that starts after the last page in the document, 
an exception will be thrown during rendering.
All ranges that end after the last page are truncated to fit in the document.


## Examples

Shows how to extract pages based on exact page indices.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Add five pages to the document.
for i in range(1, 6):
    builder.write("Page " + str(i))
    builder.insert_break(aw.BreakType.PAGE_BREAK)

# Create an "XpsSaveOptions" object, which we can pass to the document's "save" method
# to modify how that method converts the document to .XPS.
xps_options = aw.saving.XpsSaveOptions()

# Use the "page_set" property to select a set of the document's pages to save to output XPS.
# In this case, we will choose, via a zero-based index, only three pages: page 1, page 2, and page 4.
xps_options.page_set = aw.saving.PageSet([0, 1, 3])

doc.save(ARTIFACTS_DIR + "XpsSaveOptions.export_exact_pages.xps", xps_options)
```

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

## See Also

* module [aspose.words.saving](../../)
* class [PageSet](../)

