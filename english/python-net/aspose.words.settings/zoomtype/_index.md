---
title: ZoomType enumeration
linktitle: ZoomType enumeration
articleTitle: ZoomType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.settings.ZoomType enumeration. Possible values for how large or small the document appears on the screen in Microsoft Word."
type: docs
weight: 220
url: /python-net/aspose.words.settings/zoomtype/
---

## ZoomType enumeration

Possible values for how large or small the document appears on the screen in Microsoft Word.


### Members

| Name | Description |
| --- | --- |
| CUSTOM | Zoom percentage is set explicitly. It is not recalculated automatically when control size changes. |
| NONE | Indicates to use the explicit zoom percentage. Same as [ZoomType.CUSTOM](./#CUSTOM). |
| FULL_PAGE | Zoom percentage is automatically recalculated to fit one full page. |
| PAGE_WIDTH | Zoom percentage is automatically recalculated to fit page width. |
| TEXT_FIT | Zoom percentage is automatically recalculated to fit text. |

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

### See Also

* module [aspose.words.settings](../)
* class [ViewOptions](../viewoptions/)
* property [ViewOptions.zoom_type](../viewoptions/zoom_type/)

