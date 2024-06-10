---
title: ViewOptions.zoom_percent property
linktitle: zoom_percent property
articleTitle: zoom_percent property
second_title: Aspose.Words for Python
description: "ViewOptions.zoom_percent property. Gets or sets the percentage (between 10 and 500) at which you want to view your document."
type: docs
weight: 50
url: /python-net/aspose.words.settings/viewoptions/zoom_percent/
---

## ViewOptions.zoom_percent property

Gets or sets the percentage (between 10 and 500) at which you want to view your document.


```python
@property
def zoom_percent(self) -> int:
    ...

@zoom_percent.setter
def zoom_percent(self, value: int):
    ...

```

### Remarks

If value is 0 then this property uses 100 instead, else if value is less than 10 or greater 
than 500 this property throws.

Although Aspose.Words is able to read and write this option, its usage is application-specific. 
For example MS Word 2013 does not respect the value of this option.




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

* module [aspose.words.settings](../../)
* class [ViewOptions](../)

