---
title: view_type property
second_title: Aspose.Words for Python via .NET API Reference
description: "Controls the view mode in Microsoft Word."
type: docs
weight: 40
url: /python-net/aspose.words.settings/viewoptions/view_type/
---

## ViewOptions.view_type property

Controls the view mode in Microsoft Word.

Although Aspose.Words is able to read and write this option, its usage is application-specific. 
For example MS Word 2013 does not respect the value of this option.




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

* module [aspose.words.settings](../../)
* class [ViewOptions](../)

