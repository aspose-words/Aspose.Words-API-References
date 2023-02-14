---
title: ViewType enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Possible values for the view mode in Microsoft Word."
type: docs
weight: 200
url: /python-net/aspose.words.settings/viewtype/
---

## ViewType enumeration

Possible values for the view mode in Microsoft Word.


### Members

| Name | Description |
| --- | --- |
| NONE | The document shall be rendered in the default view of the application. |
| READING | The document shall be rendered in the default view of the application. |
| PAGE_LAYOUT | The document shall be opened in a view that displays the document as it will print. |
| OUTLINE | The document shall be rendered in a view optimized for outlining or creating long documents. |
| NORMAL | The document shall be rendered in a view optimized for outlining or creating long documents. |
| WEB | The document shall be rendered in a view mimicking the way this document would be displayed  in a web page. |

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

### See Also

* module [aspose.words.settings](../)
* class [ViewOptions](../viewoptions/)
* property [ViewOptions.view_type](../viewoptions/view_type/)

