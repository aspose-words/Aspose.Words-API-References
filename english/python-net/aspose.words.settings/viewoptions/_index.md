---
title: ViewOptions class
linktitle: ViewOptions class
articleTitle: ViewOptions class
second_title: Aspose.Words for Python
description: "aspose.words.settings.ViewOptions class. Provides various options that control how a document is shown in Microsoft Word"
type: docs
weight: 190
url: /python-net/aspose.words.settings/viewoptions/
---

## ViewOptions class

Provides various options that control how a document is shown in Microsoft Word.
To learn more, visit the [Work with Options and Appearance of Word Documents](https://docs.aspose.com/words/python-net/work-with-word-document-options-and-appearance/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [display_background_shape](./display_background_shape/) | Controls display of the background shape in print layout view. |
| [do_not_display_page_boundaries](./do_not_display_page_boundaries/) | Turns off display of the space between the top of the text and the top edge of the page. |
| [forms_design](./forms_design/) | Specifies whether the document is in forms design mode. |
| [view_type](./view_type/) | Controls the view mode in Microsoft Word. |
| [zoom_percent](./zoom_percent/) | Gets or sets the percentage (between 10 and 500) at which you want to view your document. |
| [zoom_type](./zoom_type/) | Gets or sets a zoom value based on the size of the window. |

### Examples

Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
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

* module [aspose.words.settings](../)
* class [Document](../../aspose.words/document/)
* property [Document.view_options](../../aspose.words/document/view_options/)

