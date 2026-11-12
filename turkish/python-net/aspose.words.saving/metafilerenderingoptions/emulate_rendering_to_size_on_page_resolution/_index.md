---
title: MetafileRenderingOptions.emulate_rendering_to_size_on_page_resolution property
linktitle: emulate_rendering_to_size_on_page_resolution property
articleTitle: emulate_rendering_to_size_on_page_resolution property
second_title: Aspose.Words for Python
description: "MetafileRenderingOptions.emulate_rendering_to_size_on_page_resolution property. Gets or sets the resolution in pixels per inch for the emulation of metafile rendering to the size on page."
type: docs
weight: 50
url: /tr/python-net/aspose.words.saving/metafilerenderingoptions/emulate_rendering_to_size_on_page_resolution/
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
# "PdfSaveOptions" nesnesi oluşturun; bu nesneyi belgenin "Save" metoduna geçebiliriz
# bu yöntemin belgeyi .PDF'ye nasıl dönüştürdüğünü değiştirmek için.
save_options = aw.saving.PdfSaveOptions()
# "EmulateRenderingToSizeOnPage" özelliğini "true" olarak ayarlayın
# sayfadaki metafile boyutuna göre renderlamayı taklit etmek için.
# "EmulateRenderingToSizeOnPage" özelliğini "false" olarak ayarlayın
# metafile renderlamasını piksel cinsinden varsayılan boyutuna taklit etmek için.
save_options.metafile_rendering_options.emulate_rendering_to_size_on_page = render_to_size
save_options.metafile_rendering_options.emulate_rendering_to_size_on_page_resolution = 50
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [MetafileRenderingOptions](../)

