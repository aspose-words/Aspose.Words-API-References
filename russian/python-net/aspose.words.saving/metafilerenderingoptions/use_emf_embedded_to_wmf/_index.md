---
title: MetafileRenderingOptions.use_emf_embedded_to_wmf property
linktitle: use_emf_embedded_to_wmf property
articleTitle: use_emf_embedded_to_wmf property
second_title: Aspose.Words for Python
description: "MetafileRenderingOptions.use_emf_embedded_to_wmf property. Gets or sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered."
type: docs
weight: 70
url: /ru/python-net/aspose.words.saving/metafilerenderingoptions/use_emf_embedded_to_wmf/
---

## MetafileRenderingOptions.use_emf_embedded_to_wmf property

Gets or sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered.


```python
@property
def use_emf_embedded_to_wmf(self) -> bool:
    ...

@use_emf_embedded_to_wmf.setter
def use_emf_embedded_to_wmf(self, value: bool):
    ...

```

### Remarks

WMF metafiles could contain embedded EMF data. MS Word in most cases uses embedded EMF data.
GDI+ always uses WMF data.

When this value is set to ``True``, Aspose.Words uses embedded EMF data when rendering.

When this value is set to ``False``, Aspose.Words uses WMF data when rendering.

This option is used only when metafile is rendered as vector graphics. When metafile is rendered
to bitmap, WMF data is always used.

The default value is ``True``.




### Examples

Shows how to configure Enhanced Windows Metafile-related rendering options when saving to PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'EMF.docx')
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
save_options = aw.saving.PdfSaveOptions()
# Установите свойство "EmfPlusDualRenderingMode" в значение "EmfPlusDualRenderingMode.Emf"
# чтобы отрисовывать только часть EMF двойного метафайла EMF+.
# Установите свойство "EmfPlusDualRenderingMode" в значение "EmfPlusDualRenderingMode.EmfPlus" чтобы
# чтобы отрисовывать часть EMF+ двойного метафайла EMF+.
# Установите свойство "EmfPlusDualRenderingMode" в значение "EmfPlusDualRenderingMode.EmfPlusWithFallback"
# чтобы отрисовывать часть EMF+ двойного метафайла EMF+, если поддерживаются все записи EMF+.
# В противном случае Aspose.Words отрисует часть EMF.
save_options.metafile_rendering_options.emf_plus_dual_rendering_mode = rendering_mode
# Установите свойство "UseEmfEmbeddedToWmf" в значение "true", чтобы отрисовывать встроенные данные EMF
# для метафайлов, которые мы можем отрисовывать как векторную графику.
save_options.metafile_rendering_options.use_emf_embedded_to_wmf = True
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.RenderMetafile.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [MetafileRenderingOptions](../)

