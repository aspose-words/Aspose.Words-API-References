---
title: ViewOptions.zoom_type property
linktitle: zoom_type property
articleTitle: zoom_type property
second_title: Aspose.Words for Python
description: "ViewOptions.zoom_type property. Gets or sets a zoom value based on the size of the window."
type: docs
weight: 60
url: /python-net/aspose.words.settings/viewoptions/zoom_type/
---

## ViewOptions.zoom_type property

Gets or sets a zoom value based on the size of the window.


```python
@property
def zoom_type(self) -> aspose.words.settings.ZoomType:
    ...

@zoom_type.setter
def zoom_type(self, value: aspose.words.settings.ZoomType):
    ...

```

### Examples

Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
doc.view_options.view_type = aw.settings.ViewType.PAGE_LAYOUT
doc.view_options.zoom_percent = 50
self.assertEqual(aw.settings.ZoomType.CUSTOM, doc.view_options.zoom_type)
self.assertEqual(aw.settings.ZoomType.NONE, doc.view_options.zoom_type)
doc.save(file_name=ARTIFACTS_DIR + 'ViewOptions.SetZoomPercentage.doc')
```

Shows how to set a custom zoom type, which older versions of Microsoft Word will apply to a document upon loading.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln('Hello world!')
# Set the "zoom_type" property to "ZoomType.PAGE_WIDTH" to get Microsoft Word
# to automatically zoom the document to fit the width of the page.
# Set the "zoom_type" property to "ZoomType.FULL_PAGE" to get Microsoft Word
# to automatically zoom the document to make the entire first page visible.
# Set the "zoom_type" property to "ZoomType.TEXT_FIT" to get Microsoft Word
# to automatically zoom the document to fit the inner text margins of the first page.
doc.view_options.zoom_type = zoom_type
doc.save(ARTIFACTS_DIR + 'ViewOptions.set_zoom_type.doc')
```

### See Also

* module [aspose.words.settings](../../)
* class [ViewOptions](../)

