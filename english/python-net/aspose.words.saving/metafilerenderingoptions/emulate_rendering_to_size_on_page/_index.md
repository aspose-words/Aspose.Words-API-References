---
title: MetafileRenderingOptions.emulate_rendering_to_size_on_page property
linktitle: emulate_rendering_to_size_on_page property
articleTitle: emulate_rendering_to_size_on_page property
second_title: Aspose.Words for Python
description: "MetafileRenderingOptions.emulate_rendering_to_size_on_page property. Gets or sets a value determining whether metafile rendering emulates the display of the metafile according to the size on page or the display of the metafile in its default size."
type: docs
weight: 40
url: /python-net/aspose.words.saving/metafilerenderingoptions/emulate_rendering_to_size_on_page/
---

## MetafileRenderingOptions.emulate_rendering_to_size_on_page property

Gets or sets a value determining whether metafile rendering emulates the display of the metafile according to the size on page
or the display of the metafile in its default size.


```python
@property
def emulate_rendering_to_size_on_page(self) -> bool:
    ...

@emulate_rendering_to_size_on_page.setter
def emulate_rendering_to_size_on_page(self, value: bool):
    ...

```

### Remarks

When metafiles are displayed in MS Word, some graphics may be scaled according to the actual metafile size in pixels.
I.e. even zooming may affect the metafile display.

When this value is set to ``True``, Aspose.Words emulates rendering according to the metafile size on page.
The size in pixels is calculated from the metafile size on the page and the specified [MetafileRenderingOptions.emulate_rendering_to_size_on_page_resolution](../emulate_rendering_to_size_on_page_resolution/).

When this value is set to ``False``, Aspose.Words emulates metafile rendering to its default size in pixels.

This option is used only when metafile is rendered as vector graphics.

The default value is ``True``.




### Examples

Shows how to display of the metafile according to the size on page.

```python
doc = aw.Document(MY_DIR + 'WMF with text.docx')
# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
save_options = aw.saving.PdfSaveOptions()
# Set the "EmulateRenderingToSizeOnPage" property to "true"
# to emulate rendering according to the metafile size on page.
# Set the "EmulateRenderingToSizeOnPage" property to "false"
# to emulate metafile rendering to its default size in pixels.
save_options.metafile_rendering_options.emulate_rendering_to_size_on_page = render_to_size
save_options.metafile_rendering_options.emulate_rendering_to_size_on_page_resolution = 50
doc.save(ARTIFACTS_DIR + 'PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf', save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [MetafileRenderingOptions](../)

