---
title: EmfPlusDualRenderingMode enumeration
linktitle: EmfPlusDualRenderingMode enumeration
articleTitle: EmfPlusDualRenderingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.EmfPlusDualRenderingMode enumeration. Specifies how Aspose.Words should render EMF+ Dual metafiles."
type: docs
weight: 160
url: /ru/python-net/aspose.words.saving/emfplusdualrenderingmode/
---

## EmfPlusDualRenderingMode enumeration

Specifies how Aspose.Words should render EMF+ Dual metafiles.


### Members

| Name | Description |
| --- | --- |
| EMF_PLUS_WITH_FALLBACK | Aspose.Words tries to render EMF+ part of EMF+ Dual metafile. If some of the EMF+ records are not supported then Aspose.Words renders EMF part of EMF+ Dual metafile. |
| EMF_PLUS | Aspose.Words renders EMF+ part of EMF+ Dual metafile. |
| EMF | Aspose.Words renders EMF part of EMF+ Dual metafile. |

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

* module [aspose.words.saving](../)

