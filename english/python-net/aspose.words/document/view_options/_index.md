---
title: Document.view_options property
linktitle: view_options property
articleTitle: view_options property
second_title: Aspose.Words for Python
description: "Document.view_options property. Provides options to control how the document is displayed in Microsoft Word."
type: docs
weight: 480
url: /python-net/aspose.words/document/view_options/
---

## Document.view_options property

Provides options to control how the document is displayed in Microsoft Word.


```python
@property
def view_options(self) -> aspose.words.settings.ViewOptions:
    ...

```

### Examples

Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln("Hello world!")

doc.view_options.view_type = aw.settings.ViewType.PAGE_LAYOUT
doc.view_options.zoom_percent = 50

self.assertEqual(aw.settings.ZoomType.CUSTOM, doc.view_options.zoom_type)
self.assertEqual(aw.settings.ZoomType.NONE, doc.view_options.zoom_type)

doc.save(ARTIFACTS_DIR + "ViewOptions.set_zoom_percentage.doc")
```

Shows how to set a custom zoom type, which older versions of Microsoft Word will apply to a document upon loading.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln("Hello world!")

# Set the "zoom_type" property to "ZoomType.PAGE_WIDTH" to get Microsoft Word
# to automatically zoom the document to fit the width of the page.
# Set the "zoom_type" property to "ZoomType.FULL_PAGE" to get Microsoft Word
# to automatically zoom the document to make the entire first page visible.
# Set the "zoom_type" property to "ZoomType.TEXT_FIT" to get Microsoft Word
# to automatically zoom the document to fit the inner text margins of the first page.
doc.view_options.zoom_type = zoom_type

doc.save(ARTIFACTS_DIR + "ViewOptions.set_zoom_type.doc")
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

