---
title: MetafileRenderingOptions.emulate_rendering_to_size_on_page_resolution property
linktitle: emulate_rendering_to_size_on_page_resolution property
articleTitle: emulate_rendering_to_size_on_page_resolution property
second_title: Aspose.Words for Python
description: "MetafileRenderingOptions.emulate_rendering_to_size_on_page_resolution property. Gets or sets the resolution in pixels per inch for the emulation of metafile rendering to the size on page."
type: docs
weight: 50
url: /it/python-net/aspose.words.saving/metafilerenderingoptions/emulate_rendering_to_size_on_page_resolution/
---

## MetafileRenderingOptions.emulate_rendering_to_size_on_page_resolution property

Gets or sets the resolution in pixels per inch for the emulation of metafile rendering to the size on page.


```python
@property
def emulate_rendering_to_size_on_page_resolution(self) -> int:
    ...

@emulate_rendering_to_size_on_page_resolution.setter
def emulate_rendering_to_size_on_page_resolution(self, value: int):
    ...

```

### Remarks

This option is used only when [MetafileRenderingOptions.emulate_rendering_to_size_on_page](../emulate_rendering_to_size_on_page/) is set to ``True``.

The default value is 96. This is a default display resolution. I.e. metafile rendering will emulate the display of
the metafile in MS Word with a 100% zoom factor.




### Examples

Shows how to display of the metafile according to the size on page.

```python
doc = aw.Document(file_name=MY_DIR + 'WMF with text.docx')
# Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo converte il documento in .PDF.
save_options = aw.saving.PdfSaveOptions()
# Imposta la proprietà "EmulateRenderingToSizeOnPage" su "true"
# per emulare il rendering in base alle dimensioni del metafile sulla pagina.
# Imposta la proprietà "EmulateRenderingToSizeOnPage" su "false"
# per emulare il rendering del metafile alla sua dimensione predefinita in pixel.
save_options.metafile_rendering_options.emulate_rendering_to_size_on_page = render_to_size
save_options.metafile_rendering_options.emulate_rendering_to_size_on_page_resolution = 50
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [MetafileRenderingOptions](../)

